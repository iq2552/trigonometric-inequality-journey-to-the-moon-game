# AAPL — Apple Inc. Stock Brief

## 1. Company snapshot

Apple ออกแบบ ผลิต และขายฮาร์ดแวร์เป็นหลัก — iPhone, Mac, iPad, Apple Watch, AirPods, Vision Pro — แล้วผูกลูกค้าไว้กับซอฟต์แวร์และบริการของตัวเอง (Advertising, AppleCare, Cloud Services) ลูกค้าคือผู้บริโภคทั่วไปที่ยอมจ่ายแพงกว่าคู่แข่งเพื่อแลกกับ ecosystem ที่ใช้งานลื่นและแบรนด์ที่ไว้ใจได้ รอบปีงบการเงินของบริษัทสิ้นสุดวันเสาร์สุดท้ายของเดือนกันยายน (source: sources/AAPL/10-k-fy2025.md) รายได้หลักมาจากไหนแน่ชัดแค่ไหน (สัดส่วน iPhone vs Services) ยังตรวจสอบไม่ได้จากไฟล์ 10-K ที่มีอยู่ตอนนี้ เพราะไฟล์เป็นแค่ excerpt เปิดเรื่อง ไม่มีตารางรายได้

## 2. Fundamentals signal

- **ไม่สามารถประเมิน revenue trend / margin trend / balance sheet / capital allocation ได้จากไฟล์ 10-K ที่มีอยู่** — ไฟล์ `sources/AAPL/10-k-fy2025.md` มีแค่ business description กับย่อหน้าเปิดของ MD&A ไม่มีงบการเงิน (income statement, balance sheet, cash flow) เลย (source: sources/AAPL/10-k-fy2025.md)
- สัญญาณเดียวที่พอมี มาจาก earnings call ไม่ใช่ 10-K: gross margin ไตรมาสล่าสุด (Q3 FY2026) ลดจาก 49.3% → 48.1% และ guidance ไตรมาสถัดไปลดต่อไปที่ midpoint ~46.5% สาเหตุหลักคือต้นทุน memory chip ที่สูงขึ้น (source: sources/AAPL/q1-2026-call.md)
- ต้องหาไฟล์ 10-K ฉบับที่มีตัวเลขงบการเงินครบ (Consolidated Statements) มาเพิ่มใน `sources/AAPL/` ก่อนถึงจะประเมิน fundamentals แบบ value investing ได้จริง — ตอนนี้ยังทำไม่ได้อย่างซื่อสัตย์

## 3. Latest earnings

**Source:** อ่านจากไฟล์เดียวที่มีใน `sources/AAPL/`: `q1-2026-call.md` — หมายเหตุ: ชื่อไฟล์บอกว่า Q1 2026 แต่เนื้อหาข้างในระบุว่าเป็น **Q3 FY2026** (front matter: `quarter: Q3 FY2026`) และเป็นแค่ excerpt สั้นจากช่วง Q&A ไม่ใช่ transcript เต็ม ไม่มีตัวเลข revenue/EPS/unit sales

- Gross margin รวมลดลงจาก 49.3% (ไตรมาสมีนาคม) เหลือ 48.1% (ไตรมาสมิถุนายน หลังปรับผล tariff refund) ลดลง 120 basis points โดยมากกว่า 100% ของการเปลี่ยนแปลงมาจากต้นทุน memory ที่สูงขึ้น ไม่ใช่ FX (source: sources/AAPL/q1-2026-call.md)
- มี partial offset จาก inventory carry benefit, ต้นทุนชิ้นส่วนที่ไม่ใช่ memory ที่ลดลง, และ product mix ที่ดีขึ้น (source: sources/AAPL/q1-2026-call.md)
- Guidance ไตรมาสถัดไป (กันยายน) อยู่ที่ midpoint ~46.5% (ไม่รวม tariff refund) ลดลงอีก 160 basis points สาเหตุหลักยังเป็นต้นทุน memory เช่นเดิม (source: sources/AAPL/q1-2026-call.md)
- Tim Cook พูดถึง Apple Intelligence/Siri: ในสหภาพยุโรปยังเปิด Siri AI บน iPhone/iPad เต็มรูปแบบไม่ได้เพราะกฎระเบียบ กำลังทำงานร่วมกับ EU Commission ส่วน Mac เปิดได้เพราะไม่อยู่ภายใต้กฎเดียวกัน (source: sources/AAPL/q1-2026-call.md)
- ในจีน เพิ่งได้รับอนุมัติให้เริ่ม ship ฟีเจอร์ Apple Intelligence พื้นฐานเมื่อสัปดาห์ก่อนวันประชุม ส่วน Siri AI เต็มรูปแบบยังต้องใช้เวลาเพิ่มเติม (source: sources/AAPL/q1-2026-call.md)

## 4. Bull case / Bear case

**Bull Case**
- ลูกค้าที่อยู่ใน ecosystem ของ Apple (iPhone + Mac + Watch + Services) มี switching cost สูง เพราะย้ายแพลตฟอร์มต้องเสียทั้งข้อมูล แอป และความคุ้นเคย
- แบรนด์ Apple แข็งแรงพอที่จะตั้งราคาพรีเมียมได้ต่อเนื่อง — สะท้อนจากยอดขาย iPhone 17 ที่ analyst มองว่ายังแข็งแรง และ Apple เพิ่งทะลุยอดขาย $10 พันล้านในอินเดีย (source: web search 2026-08-09)
- Q3 FY2026 iPhone sales รายงานว่าโต 22% ตามข่าวผลประกอบการ (source: web search 2026-08-09) — ต้อง verify ตัวเลขนี้กับ 10-K/transcript ฉบับเต็มอีกครั้งเพราะ source หลักที่อ่านได้ในโปรเจกต์ยังไม่มีตัวเลขนี้โดยตรง

**Bear Case**
- Gross margin กำลังโดนกดดันจากต้นทุน memory chip ที่สูงขึ้นจริง และ guidance เองก็บอกว่าไตรมาสถัดไปจะแย่กว่านี้อีก (source: sources/AAPL/q1-2026-call.md) — นักวิเคราะห์อย่าง Phillip Capital และ GF Securities ปรับลด rating ด้วยเหตุผลเดียวกันในสัปดาห์นี้ (source: web search 2026-08-09)
- Apple ยังเปิด Siri AI เต็มรูปแบบในตลาดสำคัญอย่าง EU และจีนไม่ได้ เพราะติด regulation (source: sources/AAPL/q1-2026-call.md) — ถ้าคู่แข่งเปิด AI feature ได้เร็วกว่าในตลาดเหล่านี้ อาจกระทบความน่าดึงดูดของ ecosystem
- มีคดี trade secrets lawsuit ระหว่าง Apple กับ OpenAI ที่ยังดำเนินอยู่ รายละเอียดผลลัพธ์ยังไม่ชัดเจนจากข้อมูลที่หาได้ (source: web search 2026-08-09)

## 5. Kill conditions

- Gross margin ลดลงต่อเนื่อง 3 ไตรมาสติด จากสาเหตุต้นทุน component (ไม่ใช่แค่ one-time) — สัญญาณว่า pricing power กำลังถูกกัดกร่อนจริง
- ผ่านไปหลายไตรมาสแล้ว Apple ยังเปิด Siri AI เต็มรูปแบบใน EU หรือจีนไม่ได้ ขณะที่คู่แข่งเปิดให้ใช้ AI feature ได้แล้วในตลาดเหล่านั้น
- ยอดขาย iPhone ในจีนหดตัวรุนแรงต่อเนื่องหลายไตรมาส โดยไม่มีสัญญาณฟื้นตัวจากสินค้าใหม่

## 6. What to ask before owning it

1. ต้นทุน memory ที่กดดัน margin ตอนนี้เป็นปัญหาชั่วคราว (cyclical) หรือโครงสร้างระยะยาว?
2. รายได้จริงแบ่งเป็นสัดส่วน iPhone vs Services เท่าไหร่ และ trend เปลี่ยนไปทางไหนในช่วง 2-3 ปีที่ผ่านมา? (ต้องหาไฟล์ 10-K ฉบับเต็มมาตอบ)
3. ถ้า Apple เปิด Siri AI เต็มรูปแบบใน EU/จีนไม่ทันคู่แข่ง จะกระทบ ecosystem lock-in ที่เป็นจุดแข็งหลักแค่ไหน?
4. งบดุลและ capital allocation (buyback, dividend, debt) เป็นยังไง — ยังตรวจสอบไม่ได้จาก source ที่มีตอนนี้
5. ราคาที่จะซื้อวันนี้ สะท้อนการเติบโตที่เชื่อว่าจะเกิดขึ้นจริงในอีก 3-5 ปีหรือยัง?

---
*Brief นี้เป็นสรุปข้อมูลเพื่อการวิจัยเท่านั้น ไม่ใช่คำแนะนำในการซื้อ/ขาย*
