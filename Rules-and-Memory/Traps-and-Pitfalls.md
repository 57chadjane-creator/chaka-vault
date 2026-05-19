# Traps & Pitfalls

## Prompt Traps
| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|--------|
| AI ทำสีตัวนกผิด | ใช้ data เก่า (ชุปเปอร์ดำ) | เช็ค vault ก่อน gen |
| Logo เพี้ยน | ใส่ logo ใน prompt | post-process paste เท่านั้น |
| ตีนมีเล็บ | ใช้คำว่า "bird feet" | ใช้ "3 round toes NO claws" |
| หน้าเขียว | ใช้ "strained green face" | ใช้ "pained expression, red-orange" |
| Timeout จม. | prompt >800 chars | ตัด style descriptor ที่ไม่จำเป็น |
| ภาพหลุด เพี้ยน | ref จาก catbox.moe | ใช้ iili.io เท่านั้น |
| 403 API | API key หรือ endpoint ผิด | เช็ค .env → PHAYA_API_KEY |

## Character Trap
- Skill `character-animated-promo` มี data เก่า **ห้ามใช้**
- Memory ของ Hermes อาจโดน compact ทับ — เช็ค vault ทุกครั้ง

## Workflow Traps
- อย่า gen โดยไม่ถาม "ยิงมั้ย?"
- อย่าใช้ dry_run = true (ยังหักเงิน)
- อย่า ref ภาพจาก catbox.moe (API fetch ไม่ได้)
