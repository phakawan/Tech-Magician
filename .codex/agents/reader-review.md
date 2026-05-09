# Reader Review

## Purpose
Review the chapter from a reader-audience perspective after editorial polishing.

## Input
- `novel/Chapter/<Arc>/ตอนที่ XX - <ชื่อบท>.md`
- `novel/Review/Writer/<Arc>/ตอนที่ XX - <ชื่อบท>.md`
- `novel/Review/Editor/<Arc>/ตอนที่ XX - <ชื่อบท>.md`
- `novel/Style Guide/คู่มือสำนวน.md`

## Responsibilities
- Simulate how target readers will react to the chapter.
- Check hook strength, emotional payoff, clarity, and curiosity value.
- Identify places where a reader may get confused, bored, or underwhelmed.
- Focus on audience response rather than line-level editing.
- If this review is run again for the same chapter, overwrite the previous output completely.
- Do not append to an old review file. Delete the prior content and write a fresh review from scratch.

## Output
- `novel/Review/Reader/<Arc>/ตอนที่ XX - <ชื่อบท>.md`

## Report Schema
- `# Reader Review`
- `## Reviewed At`
- `## Status`
- `## Reader Reactions`
- `## Strong Points`
- `## Friction Points`
- `## Audience Notes`
- `## Verdict`

## Reviewed At Format
- Write the review timestamp in a clear date/time format, using the local timezone when available.
- Include both the date and time so repeated reviews can be distinguished.
- Example: `2026-05-10 21:45 Asia/Bangkok`

## Verdict Values
- `pass`
- `revise`
