# AI Novel Multi-Agent

ระบบนี้มีเอเจนต์ 15 ตัวสำหรับเขียนนิยายแบบมีโครง ตรวจคุณภาพ และประเมินผลเชิงผู้อ่านก่อนส่งออก

## Agents

1. Story Architect
- กำหนด genre, theme, premise, tone, ending และ chapter arc
- ส่งออก: `story_bible`

2. Character Designer
- ออกแบบตัวละครหลักและความสัมพันธ์
- ส่งออก: `character_bible`

3. Worldbuilding Agent
- สร้างระบบโลก กฎ สถานที่ ประวัติศาสตร์ และ timeline โลก
- ส่งออก: `world_bible`, `world_rules`, `world_timeline`

4. Plot Planner
- แตกโครงเป็น chapter beats และ scene cards
- ส่งออก: `chapter_plan`, `scene_cards`

5. Scene Writer
- เขียนฉากจาก scene card โดยไม่แก้ canon
- ต้องยึด `novel/Style Guide/คู่มือสำนวน.md`
- ส่งออก: `scene_draft`

6. Continuity Checker
- ตรวจความต่อเนื่องกับ canon และ timeline
- ส่งออก: `continuity_report`

7. Fact Research Agent
- ตรวจความถูกต้องของข้อมูลจริงที่อิงประวัติศาสตร์ วิทยาศาสตร์ การแพทย์ กฎหมาย ฯลฯ
- ส่งออก: `fact_report`

8. Critic Agent
- วิจารณ์เชิงโครงเรื่อง จังหวะ conflict และ hook
- ส่งออก: `critic_report`

9. Reader Persona Agent
- จำลองมุมมองผู้อ่านหลายกลุ่มและประเมินผลตอบรับ
- ส่งออก: `reader_response_report`

10. Editor Stylist
- ปรับภาษา โทน จังหวะ และความลื่นไหล
- ต้องตรวจตาม `novel/Style Guide/คู่มือสำนวน.md`
- ส่งออก: `final_scene`

11. Thai Fiction Direct Polish
- โหมด rewrite ตรงสำหรับงานภาษาไทยนิยายโดยเฉพาะ
- ใช้ `thai-fiction-direct-polish` เป็นพฤติกรรมหลัก
- ส่งออก: `polished_scene`

12. Novel Writer
- เขียนบท/ตอนที่สมบูรณ์และบันทึกเป็นไฟล์ Markdown ใน `novel/Chapter/`
- ต้องยึด `novel/Style Guide/คู่มือสำนวน.md`
- ส่งออก: `novel/Chapter/<Arc>/ตอนที่ XX - <ชื่อบท>.md`

13. Writer Review
- ตรวจบทจากมุมมองผู้เขียนก่อนส่งเข้ารอบแก้เชิงสำนวน
- ต้องยึด `novel/Style Guide/คู่มือสำนวน.md`
- ส่งออก: `novel/Review/Writer/<Arc>/ตอนที่ XX - <ชื่อบท>.md`

14. Editor Review
- ตรวจบทที่ขัดเกลาแล้วก่อนยืนยันความพร้อมใช้งาน
- ต้องยึด `novel/Style Guide/คู่มือสำนวน.md`
- ส่งออก: `novel/Review/Editor/<Arc>/ตอนที่ XX - <ชื่อบท>.md`

15. Reader Review
- จำลองมุมมองผู้อ่านหลังบทผ่านการขัดเกลา
- ต้องยึด `novel/Style Guide/คู่มือสำนวน.md`
- ส่งออก: `novel/Review/Reader/<Arc>/ตอนที่ XX - <ชื่อบท>.md`

## Pipeline

`Story Architect -> Character Designer -> Worldbuilding Agent -> Plot Planner -> Novel Writer -> Continuity Checker -> Fact Research Agent -> Critic Agent -> Reader Persona Agent -> Editor Stylist -> Thai Fiction Direct Polish -> Writer Review -> Editor Review -> Reader Review`

## Shared References

- `novel/Story Bible/` สำหรับ canon หลัก
- `novel/Chapter Memory/` สำหรับสรุประดับบท
- `novel/Scene Memory/` สำหรับสรุประดับฉาก
- `novel/Style Guide/คู่มือสำนวน.md` สำหรับมาตรฐานภาษา
- `novel/Workflow/เวิร์กโฟลว์การเขียนนิยาย.md` สำหรับลำดับการทำงานมาตรฐาน

## Ground Rules

- ใช้ `story_bible`, `character_bible`, `world_rules`, `timeline_facts`, และ style guide เป็น source of truth
- เอเจนต์ทุกตัวแก้ canon ไม่ได้โดยตรง ให้เสนอ `change_proposal`
- ถ้า `Continuity Checker` พบ conflict ระดับบล็อก ต้องย้อนกลับไปแก้ก่อนส่ง Editor
