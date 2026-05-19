# Pipeline — ผลิตคลิปการ์ตูนโปรโมท

## 1. Gen ภาพ keyframe (Phaya Nano Banana)
- **Endpoint:** `POST /api/v1/nano-banana/create`
- **Cost:** 2 THB/ภาพ (1K, 16:9)
- **Refs:** ใส่ `image_input` เสมอ — ทั้ง 3 ตัวละคร + ป้าย/asset
- **Poll:** `GET /api/v1/nano-banana/status/{job_id}`
- **Format:** aspect_ratio=16:9, resolution=1K, output_format=jpg

## 2. Rules
- ✅ **โลโก้ชกา ต้องอยู่ใน BG ทุกภาพ** — โปรโมททางอ้อม
- ✅ ใช้ข้อมูลตัวละครจาก Obsidian vault (Characters/) — ห้ามใช้ data เก่า
- ✅ ALL 3 ref URL ใน image_input ทุกรอบ
- ✅ ถาม "ยิงมั้ย?" ก่อน gen ทุกครั้ง
- ❌ ห้ามรวม logo ใน prompt text — ใช้ post-processing paste ทีหลัง

## 3. Workflow Flow
1. รับ brief → เช็ค vault ตัวละคร
2. Craft prompt → โชว์ให้ดู → ถาม "ยิงมั้ย?"
3. ยิง → ดู result → ส่งให้ approve
4. ถ้า OK → save → next
5. ถ้า NG → หา root cause → แก้ prompt → ยิงใหม่

## Refs ที่ต้องมีทุกครั้ง
- ลุงชู: https://iili.io/By7iIne.jpg
- ชุปเปอร์: https://iili.io/ByA91QS.jpg
- ชิบเปอร์: https://iili.io/By5DWEF.jpg
