---
name: math-brief
description: Use when the user asks for a study brief on a math topic (e.g. "/math อนุพันธ์", "ทำ brief เรื่อง matrix ให้หน่อย"). Outputs a 5-section markdown brief (with step-by-step problem solutions) saved to briefs-math/<TOPIC>.md.
---

# math-brief SOP

## When to use this

ผู้ใช้ขอสรุป/brief เรื่อง math 1 หัวข้อ trigger ทั่วไป:
- `/math <TOPIC>` slash command
- "ทำ brief เรื่อง X ให้หน่อย"
- "สรุปเรื่อง X (คณิต) ให้หน่อย"

## Inputs you need

- 1 หัวข้อ math (TOPIC) เช่น "อนุพันธ์", "matrix", "integration by parts"
- ถ้าไม่มี topic ให้ ask ก่อนเริ่มทำ

## Steps

1. Confirm topic ถ้า ambiguous ให้ ask user ยืนยัน
2. Dispatch sub-agent ทั้ง 3 ตัว by name ในข้อความเดียวกัน (ห้าม dispatch ทีละตัว ต้องรันขนาน):
   - **Reze-Math** → อ่าน `sources/math_Grade 12/<TOPIC>/` เฉพาะไฟล์เนื้อหา/ตำราที่มีวันที่แก้ไขล่าสุด (ถ้าหลายไฟล์วันเดียวกันอ่านทุกไฟล์) → return สรุปเนื้อหาหลัก + สูตร/ทฤษฎีบทสำคัญ
   - **Megumin-Math** → อ่าน `sources/math_Grade 12/<TOPIC>/` เฉพาะไฟล์โจทย์/แบบฝึกหัดที่มีวันที่แก้ไขล่าสุด (ถ้าหลายไฟล์วันเดียวกันอ่านทุกไฟล์) → return ตัวอย่างโจทย์ พร้อมวิธีทำแบบ step-by-step ครบทุกขั้นตอน + จุดที่มักผิด + แนวข้อสอบ
   - **Rem-Math** → ใช้ WebSearch → return คำอธิบาย/ตัวอย่างจากอินเตอร์เน็ต + แหล่งเรียนเพิ่มเติม
3. รวมผลลัพธ์จาก Reze-Math, Megumin-Math, Rem-Math เข้ากับ output format ด้านล่าง ถ้า agent ไหน report ว่าไม่เจอ source ให้สะท้อนตรงๆ ในผลลัพธ์ (เช่น "ไม่มีไฟล์เนื้อหาใน sources/math_Grade 12/<TOPIC>/") ห้ามเติมข้อมูลจากความจำแทน `sources/math_Grade 12/` เป็น folder เฉพาะของ math แยกจาก `sources/<TICKER>/` ที่ /brief ใช้ ห้ามข้ามไปอ่าน folder ของหุ้น
4. ถ้า folder `briefs-math/` ยังไม่มี ให้สร้าง
5. Save brief ที่ `briefs-math/<TOPIC>.md`
6. แสดง brief เต็มกลับใน chat ด้วย

## Output format (5 sections, required, no skipping)

### 1. วิธีใช้
สูตร/ขั้นตอนการใช้งาน เป็น bullet points (source: Reze-Math ถ้ามีไฟล์เนื้อหา ไม่งั้น fallback ไป Rem-Math)

### 2. ตัวอย่างโจทย์
2-4 ตัวอย่าง **ต้องมีวิธีทำแบบ step-by-step ครบทุกขั้นตอน** ไม่ใช่แค่คำตอบสุดท้าย (source: Megumin-Math) ถ้า source มีเฉลยอยู่แล้วให้ยึดตามเฉลยนั้น ถ้า source ไม่มีเฉลย (มีแต่โจทย์เปล่า) ให้คำนวณเองตามกฎคณิตศาสตร์มาตรฐานได้ แต่ต้องระบุชัดเจนว่า "วิธีทำนี้คำนวณเอง ไม่ใช่เฉลยจาก source" ถ้า folder ว่างหรือไม่มีไฟล์โจทย์ เขียนตรงๆ ว่า "ไม่มีไฟล์โจทย์ใน sources/math_Grade 12/<TOPIC>/"

### 3. จุดที่มักผิด
2-4 bullets (source: Megumin-Math)

### 4. แนวข้อสอบ
2-3 bullets รูปแบบโจทย์ที่มักออกสอบ (source: Megumin-Math + Rem-Math)

### 5. แหล่งเรียนเพิ่ม
2-4 bullets ชื่อแหล่ง/ลิงก์อ้างอิงจากอินเตอร์เน็ต (source: Rem-Math)

## Voice rules

- ภาษาเข้าใจง่าย เหมาะกับคนกำลังเรียน ไม่ใช้ศัพท์เทคนิคเกินจำเป็นโดยไม่อธิบาย
- ห้ามแต่งโจทย์/สูตร/ลิงก์ที่ไม่มี source รองรับ
- ถ้าไม่แน่ใจ บอกตรงๆ ว่าไม่แน่ใจ ดีกว่าแต่ง

## When unsure

Honest > confident ถ้าข้อมูลไม่พอ พูดว่า "ผมไม่แน่ใจ ลองดูใน [source]" ดีกว่าแต่ง
