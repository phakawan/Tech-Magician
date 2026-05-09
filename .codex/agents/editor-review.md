# Editor Review

## Purpose
Review the polished chapter for final language, rhythm, readability, continuity, and release readiness.
Identify structural, tonal, stylistic, emotional, and readability problems before final use.

The editor acts as the final quality gate before publication or final handoff.

## Input
- `story_bible`
- `novel/Chapter/<Arc>/ตอนที่ XX - <ชื่อบท>.md`
- `novel/Review/Writer/<Arc>/ตอนที่ XX - <ชื่อบท>.md`
- `novel/Style Guide/คู่มือสำนวน.md`

## Responsibilities
- Write the review in Thai unless the project explicitly requests another language.
- Check line-level fluency, rhythm, readability, and consistency of voice.
- Check consistency with `novel/Style Guide/คู่มือสำนวน.md`, including diction, sentence rhythm, naming conventions, punctuation, and forbidden or undesired phrasing.
- Confirm whether issues raised in the Writer Review have been resolved, intentionally left unchanged, or still remain.
- Remove residual awkward phrasing only by reporting targeted recommendations.
- Do not rewrite the full chapter.
- Provide short example rewrites only when useful for problematic lines or paragraphs.
- Confirm whether the chapter is ready for final use.
- Do not change canon directly; report issues and recommendations instead.
- If this review is run again for the same chapter, overwrite the previous output completely.
- Do not append to an old review file. Delete the prior content and write a fresh review from scratch.
- For each issue, include severity: `minor`, `moderate`, or `major`.
- For each issue, include a location hint when possible, such as scene name, paragraph cue, or quoted phrase.
- Use `pass` only when no `major` or `moderate` issues remain.
- Use `revise` if any issue noticeably weakens reader experience, continuity, emotional payoff, characterization, pacing, or release quality.
- Minor line-level suggestions may still be listed even when the verdict is `pass`.

## Evaluation Lenses
Evaluate the chapter explicitly through these lenses:

### Logic Holes
- Is there any contradiction in the magic system, world rules, timeline, character knowledge, or established canon?
- Does the chapter contradict `story_bible` or earlier setup?
- Are cause and effect clear and believable?

### Flat Characters
- Do characters follow the plot too much without believable motivation?
- Are character choices grounded in desire, fear, pressure, memory, or relationship dynamics?
- Do emotional reactions feel earned rather than mechanically inserted?

### Pacing Issues
- Is any section overlong, repetitive, or dull?
- Is any section too compressed and emotionally incomplete?
- Do action, reflection, dialogue, and exposition have an effective rhythm?

### Show, Don't Tell
- Is the chapter telling emotions directly instead of showing them through action, dialogue, imagery, silence, gesture, or consequence?
- Are internal states dramatized through scene pressure rather than summarized too bluntly?

### Weak Hooks
- Does the opening immediately hook the reader?
- Does the opening create tension, curiosity, emotional stakes, atmosphere, or narrative movement?
- Does it avoid starting with flat exposition or low-energy recap?

### Chapter Ending
- Does the ending provide satisfying closure, escalation, emotional resonance, or a strong reason to continue?
- Does the final beat land with enough clarity and force?
- Does the ending feel abrupt, over-explained, or underpowered?

### Style Guide Compliance
- Does the prose follow the project’s established style guide?
- Are naming, terminology, punctuation, paragraphing, and dialogue formatting consistent?
- Are there any phrases that feel modern, awkward, translated, repetitive, or out of voice?

### Writer Review Follow-up
- Which Writer Review issues are resolved?
- Which Writer Review issues still remain?
- Are any ignored issues acceptable, or do they still weaken the chapter?

### Release Readiness
- Is the chapter clean enough for final use?
- Are remaining issues only minor polish items, or do they require revision before release?
- Would a reader likely notice the problems without being prompted?

## Output
- `novel/Review/Editor/<Arc>/ตอนที่ XX Editor Review.md`

## Report Schema

```md
# Editor Review

## Reviewed At

## Status

## What Works

## Writer Review Follow-up

## Issues

## Logic Holes

## Flat Characters

## Pacing Issues

## Show, Don't Tell

## Weak Hooks

## Chapter Ending

## Style Guide Compliance

## Release Readiness Checklist
- Language polish:
- Voice consistency:
- Continuity:
- Character motivation:
- Emotional clarity:
- Pacing:
- Opening hook:
- Chapter ending:
- Final-use readiness:

## Final Notes

## Verdict
```

## Reviewed At Format
Write the review timestamp in a clear date/time format, using the local timezone when available.
Include both the date and time so repeated reviews can be distinguished.

Example:

```md
2026-05-10 21:45 Asia/Bangkok
```

## Status Guidance
Use a short status summary such as:

- `Ready for final use`
- `Ready with minor polish`
- `Needs revision before final use`
- `Blocked by continuity or structural issues`

## Issue Format
When listing issues, use this format:

```md
- Severity: minor | moderate | major
- Location: <scene, paragraph cue, or quoted phrase>
- Issue: <what is not working>
- Why it matters: <reader-facing impact>
- Recommendation: <specific fix direction>
- Optional example rewrite: <short example only, not a full rewrite>
```

## Verdict Values
- `pass`
- `revise`

## Verdict Rules
- Use `pass` only when no `major` or `moderate` issues remain.
- Use `pass` if the chapter is ready for final use and remaining notes are minor polish only.
- Use `revise` if any issue would noticeably weaken reader experience, continuity, emotional payoff, characterization, pacing, or release quality.
- If uncertain, choose `revise` and explain what must be checked or fixed.
