# Review Workflow

## Purpose
Review completed chapters in three passes:
1. Writer-side structural review
2. Editor-side language review
3. Reader-side audience review

This workflow is used after `Novel Writer` produces a chapter under `novel/Chapter/`.

## Review Agents

### 1. Writer Review
- Agent: `writer-review`
- Purpose: check chapter shape, scene delivery, pacing, and canon-risk before polishing or release
- Input: completed chapter, style guide, relevant canon
- Output: `novel/Review/Writer/<Arc>/ตอนที่ XX - <ชื่อบท>.md`
- Verdict values: `pass`, `revise`

### 2. Editor Review
- Agent: `editor-review`
- Purpose: check line-level fluency, rhythm, consistency of voice, and final readability
- Input: completed chapter, writer review, style guide
- Output: `novel/Review/Editor/<Arc>/ตอนที่ XX - <ชื่อบท>.md`
- Verdict values: `pass`, `revise`

### 3. Reader Review
- Agent: `reader-review`
- Purpose: simulate reader reaction after editorial polish
- Input: completed chapter, writer review, editor review, style guide
- Output: `novel/Review/Reader/<Arc>/ตอนที่ XX - <ชื่อบท>.md`
- Verdict values: `pass`, `revise`

## Workflow Order

1. Run `Writer Review` on the completed chapter.
2. If `Writer Review` returns `revise`, revise the chapter before proceeding.
3. Run `Editor Review` on the revised or polished chapter.
4. If `Editor Review` returns `revise`, revise the chapter again before proceeding.
5. Run `Reader Review` on the final polished chapter.
6. If `Reader Review` returns `revise`, decide whether to:
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

## Recommended Use

Use this workflow whenever a chapter is ready to move from drafting into quality control and audience validation.

