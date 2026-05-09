---
name: thai-fiction-direct-polish
description: Directly polish Thai fiction prose into natural, fluent Thai without waiting for approval. Use for Thai novels, scene rewrites, prose smoothing, translated-sounding phrasing cleanup, line-level Thai fiction editing, and requests phrased like "read and polish this chapter/scene" or "อ่านและเกลาตอนที่...".
---

# Thai Fiction Direct Polish

## Purpose
Use this skill to directly rewrite Thai fiction so it reads naturally, smoothly, and emotionally true in Thai.

This skill is for execution, not just commentary.
Default behavior is to produce a polished rewrite immediately unless the user explicitly asks for review-only feedback.

## Use this skill when
Use this skill when the user asks to:
- polish Thai fiction
- smooth prose
- rewrite awkward Thai
- remove translated-sounding phrasing
- fix unnatural wording
- proofread Thai novel text
- make dialogue sound more natural
- rewrite a scene or chapter in better Thai


## Default mode
Default to **direct rewrite**.

Do not stop at critique unless the user explicitly asks for:
- review only
- score only
- what should be fixed without rewriting
- approval before rewriting

If the request is ambiguous between critique and rewrite, prefer rewrite.

## Core editing goals
1. Make the prose sound naturally Thai.
2. Remove translated or overly literal sentence structure.
3. Preserve original meaning.
4. Preserve scene tension, tone, and pacing.
5. Preserve character voice.
6. Avoid over-beautifying simple prose.
7. Avoid rewriting so much that the text becomes a different story.

## Editing rules
- Keep the original scene content intact unless the user asks for expansion or reduction.
- Preserve emotional intent.
- Preserve important repetitions if they are clearly stylistic.
- Cut repetition only when it weakens rhythm unintentionally.
- Prefer the smallest effective change first.
- If dialogue already works, do not flatten it.
- If a line is intentionally blunt, keep it blunt.
- If a character sounds sharp, tired, cold, warm, childish, or restrained, preserve that texture.

## What to improve
Look for:
- translated-sounding syntax
- stiff or unnatural Thai
- over-explained sentences
- abstract lines that feel mentally translated
- dialogue that sounds like narration
- repeated filler words
- broken emotional rhythm
- sentence endings that feel too literal
- mismatched tone within the same scene

## What not to do
- Do not turn every sentence literary.
- Do not replace simple good Thai with fancy Thai.
- Do not erase character personality.
- Do not make every character speak in the same voice.
- Do not insert new plot information.
- Do not moralize or critique unless asked.
- Do not ask for approval before rewriting unless the user explicitly wants approval first.

## Output formats
Choose the output that best matches the user's request.

### A. Full rewrite
Use when the user shares a passage or chapter and wants it polished.
Return the rewritten Thai text directly.

### B. Line-by-line replacement
Use when the user wants problem spots identified.
Format:
Original:
Better:
Why: short and optional

### C. Targeted rewrite
Use when the user asks to fix only certain lines, dialogue, narration, or a specific paragraph.

## Style target
The ideal result should feel:
- fluent
- natural
- Thai-first rather than translated
- emotionally precise
- easy to read aloud
- true to the original story voice

## Quality bar before returning
Before finishing, check:
- Does this sound like native Thai fiction prose?
- Did I preserve the emotional shape of the scene?
- Did I keep the character voice?
- Did I accidentally over-write?
- Did I rewrite directly instead of only commenting?

If the answer to the last question is no, rewrite the output into direct execution mode.
