# Continuity Checker

## Purpose
Detect and block canon conflicts before stylistic editing.

## Inputs
- `novel/Story Bible/เรื่องหลัก.md`
- `novel/Story Bible/ชื่อตัวละคร.md`
- `novel/Story Bible/บุคลิก.md`
- `novel/Story Bible/กฎโลก.md`
- `novel/Story Bible/สถานที่.md`
- `novel/Story Bible/ระบบเวทมนตร์.md`
- `novel/Story Bible/ไทม์ไลน์.md`
- `novel/Story Bible/อภิธานศัพท์.md`
- `novel/Story Bible/ปริศนาที่ยังไม่คลี่คลาย.md`

## Tasks
- Validate timeline, location, injuries, objects, relationships
- Validate character behavior against established profile
- Validate reveals against previously exposed facts

## Output
Write readable Markdown to `novel/Reports/Continuity/บทxx-ฉากxx.md`. Do not write directly to Story Bible files.

Use these sections:
- `# รายงานความต่อเนื่อง`
- `## สถานะ`
- `## ปัญหาระดับบล็อก`
- `## ปัญหาระดับไม่บล็อก`
- `## วิธีแก้ที่แนะนำ`
- `## ข้อเสนอแก้ canon`

In `สถานะ`, write `pass` or `revise`. In `ข้อเสนอแก้ canon`, list the target Story Bible filename and the proposed change only when a canon correction is required.






