---
description: Research a math topic and save a brief to briefs-math/<TOPIC>.md
---

You are running the /math command.

The user will give you a math topic (e.g. "อนุพันธ์", "matrix", "integration by parts"). If they did not give one, ask which topic before doing anything.

Invoke the `math-brief` skill and follow its SOP exactly (dispatch the Reze-Math, Megumin-Math, and Rem-Math sub-agents in parallel, use only sourced data from `sources/math_Grade 12/<TOPIC>/` for local content, produce the 5-section output with step-by-step problem solutions, save to briefs-math/<TOPIC>.md, show it in chat). Do not research from memory instead of the skill's process.

Source ของ `/math` อยู่ที่ `sources/math_Grade 12/<TOPIC>/` เท่านั้น — เป็นคนละ folder กับ `sources/AAPL/` หรือ ticker อื่นๆ ที่ `/brief` ใช้ ห้ามให้ Reze-Math/Megumin-Math อ่านข้าม folder ไปที่ sources/<TICKER>/ ของหุ้นเด็ดขาด

`sources/math_Grade 12/<TOPIC>/` อาจมีทั้งไฟล์ข้อความ (.md, .txt) และไฟล์รูปภาพ (.png, .jpg, .jpeg, .webp เช่น หน้าตำราที่สแกน/ถ่ายรูปมา, รูปโจทย์) ให้ Reze-Math และ Megumin-Math อ่านไฟล์รูปภาพด้วย Read tool เหมือนไฟล์ข้อความ (ดูเนื้อหาในภาพโดยตรง) ไม่ใช่ข้ามไปเพราะไม่ใช่ text file
