# Review Workflow

## Purpose
Review completed chapters in three passes:
1. Writer-side structural review
2. Editor-side language review
3. Reader-side audience review

This workflow is used after `Novel Writer` produces a chapter under `novel/Chapter/`.

## Review Selection

Before running this workflow, ask which review agents to run:
- `Writer Review`
- `Editor Review`
- `Reader Review`

The user may select one, two, or all three.
If a review is not selected, skip it entirely and do not create that report.
When multiple reviews are selected, run only the chosen agents in the standard order:
`Writer Review -> Editor Review -> Reader Review`

Suggested question:
`ต้องการให้รันรีวิวตัวไหนบ้าง: Writer Review, Editor Review, Reader Review? เลือกได้มากกว่าหนึ่งอัน`

## Review Agents

### 1. Writer Review
- Agent: `writer-review`
- Purpose: check chapter shape, scene delivery, pacing, and canon-risk before polishing or release
- Input: completed chapter, style guide, relevant canon
- Output: `novel/Review/Writer/<Arc>/ตอนที่ XX - <ชื่อบท>.md`
- Verdict values: `pass`, `revise`
- If the same chapter is reviewed again, overwrite the previous writer review file completely.
- Include a clear `Reviewed At` date/time in the report output so repeat reviews can be distinguished.

### 2. Editor Review
- Agent: `editor-review`
- Purpose: check line-level fluency, rhythm, consistency of voice, and final readability
- Input: completed chapter, writer review, style guide
- Output: `novel/Review/Editor/<Arc>/ตอนที่ XX - <ชื่อบท>.md`
- Verdict values: `pass`, `revise`
- If the same chapter is reviewed again, overwrite the previous editor review file completely.
- Include a clear `Reviewed At` date/time in the report output so repeat reviews can be distinguished.

### 3. Reader Review
- Agent: `reader-review`
- Purpose: simulate reader reaction after editorial polish
- Input: completed chapter, writer review, editor review, style guide
- Output: `novel/Review/Reader/<Arc>/ตอนที่ XX - <ชื่อบท>.md`
- Verdict values: `pass`, `revise`
- If the same chapter is reviewed again, overwrite the previous reader review file completely.
- Include a clear `Reviewed At` date/time in the report output so repeat reviews can be distinguished.

## Workflow Order

1. Ask which review agents should run.
2. Run only the selected review agents, in order.
3. If `Writer Review` returns `revise`, revise the chapter before proceeding to any later selected review.
4. If `Editor Review` returns `revise`, revise the chapter again before proceeding to any later selected review.
5. If `Reader Review` returns `revise`, decide whether to:
- return to writer/editor revision depending on the issue
- or keep the chapter as-is if the note is preference-level only

## Canon and Style Rules

- Do not let any review agent change canon directly.
- Use `story_bible`, `character_bible`, `world_rules`, `timeline_facts`, and `novel/Style Guide/คู่มือสำนวน.md` as source of truth.
- If a review finds a blocking canon issue, it must report it as a required revision, not silently fix it.

## Output Folder Layout

- `novel/Review/Writer/`
- `novel/Review/Editor/`
- `novel/Review/Reader/`

## Editor Review Re-run Rule

- When re-running `Editor Review` for the same chapter, delete the old report content and write a fresh file.
- Do not append notes to an existing report.
- Always include the new review timestamp in the report body.

## Writer and Reader Re-run Rule

- When re-running `Writer Review` or `Reader Review` for the same chapter, delete the old report content and write a fresh file.
- Do not append notes to an existing report.
- Always include the new review timestamp in the report body.

## Recommended Use

Use this workflow whenever a chapter is ready to move from drafting into quality control and audience validation.
