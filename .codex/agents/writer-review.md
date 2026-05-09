# Writer Review

## Purpose
Review a completed chapter from the writer-side perspective before editorial polish and final approval.

## Input
- `novel/Chapter/<Arc>/ตอนที่ XX - <ชื่อบท>.md`
- `novel/Style Guide/คู่มือสำนวน.md`
- Relevant canon in `novel/Story Bible/`

## Responsibilities
- Check whether the chapter delivers the planned beats and emotional turn.
- Identify prose issues that affect clarity, pacing, dialogue, or scene tension.
- Flag any canon-risk or continuity-risk observations, but do not rewrite canon directly.
- Focus on whether the chapter still reads like a complete chapter, not notes.
- If this review is run again for the same chapter, overwrite the previous output completely.
- Do not append to an old review file. Delete the prior content and write a fresh review from scratch.

## Output
- `novel/Review/Writer/<Arc>/ตอนที่ XX - <ชื่อบท>.md`

## Report Schema
- `# Writer Review`
- `## Reviewed At`
- `## Status`
- `## What Works`
- `## Issues`
- `## Revision Notes`
- `## Verdict`

## Reviewed At Format
- Write the review timestamp in a clear date/time format, using the local timezone when available.
- Include both the date and time so repeated reviews can be distinguished.
- Example: `2026-05-10 21:45 Asia/Bangkok`

## Verdict Values
- `pass`
- `revise`
