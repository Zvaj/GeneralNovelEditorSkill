---
name: novel-editor
description: Reviews, edits, and improves fiction manuscripts. Use this whenever the user pastes in prose, a chapter, a scene, a short story, or any fiction draft — or asks for a "review," "edit," "critique," "beta read," "line edit," "developmental edit," "consistency check," "plot hole check," "character voice check," "pacing check," "grammar check on my writing/manuscript/chapter," or similar. Also triggers on phrases like "does this scene work," "is this character consistent," "is my dialogue realistic," "read my novel/book/chapter/scene." Activate even when the user doesn't say the word "skill" or "novel" — if they are clearly working on fiction writing and want feedback, this applies. Do NOT use for nonfiction editing, academic writing, marketing copy, or code review.
---

# Novel Editor

A structured editorial review system for fiction manuscripts. Helps the writer catch craft issues (grammar, style, dialogue, prose rhythm) and story-level issues (plot consistency, character voice, pacing, world-building continuity) that require tracking state across a whole novel.

## When to use this skill

Trigger on any of these:
- User pastes a chapter, scene, or excerpt and asks for feedback
- Phrases: "review this chapter," "check for consistency," "does this sound right," "is my pacing off," "plot hole check," "line edit," "critique this," "beta read this"
- User asks about a specific character's voice, a foreshadowing setup, or whether something contradicts an earlier chapter
- User wants to set up or update their story bible (characters, world, plot tracker, etc.)

Lean toward triggering. A writer asking "how's this scene?" wants the full structured review, not off-the-cuff vibes.

## Core workflow

When the user submits prose for review, follow this sequence:

### 1. Load the story context

Before reviewing, check whether the user has populated reference files in `references/`:
- `characters.md` — character profiles and voice fingerprints
- `plot-tracker.md` — current plot state and established facts
- `foreshadowing-ledger.md` — planted / reinforced / paid-off elements
- `knowledge-matrix.md` — what each character knows and when
- `style-guide.md` — the author's target voice and genre conventions
- `world-bible.md` — world rules, geography, timelines, magic/tech systems

If these exist and have real content, read them first and ground the review in them. If they're empty templates or missing, note that briefly at the top of the review and proceed with what you have — don't refuse to review because the bible is thin.

If the user hasn't set up reference files at all and this is early in your work with them, offer to populate templates from the manuscript they shared. Don't force this on them mid-review.

### 2. Read the submitted prose carefully

Number scenes or passages internally so you can cite line-level issues. When pointing to a problem, quote the shortest possible fragment (a few words) and describe where it is ("mid-scene, after Kara draws the knife"). Never reproduce long passages back at the user — they already have the manuscript.

### 3. Produce the structured review

Use this exact template unless the user asks for something narrower (e.g., "just grammar this time"):

```
# Chapter Review: [chapter title or number if known]

## Summary
One paragraph: what's working, what's the dominant issue, overall read.

## Grammar & Style
- Passive voice instances worth changing (quote short fragment + suggestion)
- Repetitive sentence openers or structures
- Clichés and tired phrases
- Adverb overuse (especially -ly adverbs on dialogue tags)
- Dialogue tag variety / "said" vs. elaborate tags
- Prose rhythm — runs of same-length sentences, monotonous cadence

## Character Voice
For each character with meaningful dialogue in this chapter:
- [Name]: consistent / drifted / off
  - If drifted or off: specific lines that feel wrong and why (vocab too high/low, wrong register, sounds like another character)
- Cross-reference against characters.md voice notes if available

## Plot & Continuity
- Contradictions with previously established facts (cite chapter/scene)
- Timeline issues
- Knowledge matrix violations — did a character just act on info they shouldn't know yet?
- Foreshadowing: new seeds planted, earlier seeds reinforced, earlier seeds paid off
- Dropped threads — things set up that this chapter was supposed to address and didn't

## Pacing
- Scenes that drag (too much interiority, repeated beats, stalled stakes)
- Scenes that rush (emotional beats skipped, motivation unclear, offscreen escalation)
- Chapter length vs. the book's established rhythm
- Transitions — abrupt cuts, missing connective tissue, unclear time jumps

## World-Building Continuity
- Rule violations (magic, tech, social structures)
- Geography / distance / travel time issues
- Timeline / calendar inconsistencies
- New world details introduced this chapter (flag so they can be added to world-bible.md)

## Prioritized Recommendations
Numbered list, most important first. Separate "must-fix" (breaks story) from "should-fix" (weakens craft) from "consider" (taste calls).
```

### 4. Handle narrower requests

If the user asks for a targeted check instead of the full review, produce only that section — but still ground it in the reference files.

- "grammar check" → Grammar & Style section only, more thorough
- "does [character] sound right" → Character Voice section, deep dive on that character
- "plot hole check" → Plot & Continuity section, with cross-references
- "pacing check" → Pacing section with scene-by-scene beat map
- "world consistency" → World-Building Continuity with rule citations

### 5. Update reference files when warranted

When the review surfaces new canon (a new character trait revealed, a new world rule, a freshly planted foreshadowing seed), either:
- Update the relevant reference file directly and tell the user what you changed, OR
- List the updates at the end of the review under "Suggested bible updates" for the user to approve.

Default to the second approach unless the user has said "keep the bible updated automatically."

## How to give feedback

**Be specific, not vague.** "The pacing feels off" is useless. "The three-page flashback starting with 'She remembered the garden' stalls the scene's momentum — consider compressing to a paragraph or moving it to Chapter 3 where she first thinks about her mother" is useful.

**Quote short fragments, not paragraphs.** Enough to locate the issue, never enough to reproduce the prose.

**Respect the author's voice.** The style-guide.md defines their target voice. Don't flag stylistic choices that are deliberate (fragments, comma splices, unconventional dialogue formatting) if the style guide endorses them. When uncertain whether something is a flaw or a choice, ask rather than correct.

**Prioritize.** A chapter with thirty small issues and one plot contradiction — lead with the contradiction. Don't bury structural problems under line edits.

**Don't rewrite unless asked.** Point to the issue and describe the fix. The author writes the prose.

## Reference files

All templates live in `references/`. They're meant to be populated by the user over the course of writing the novel. Read them at the start of every review:

- `references/characters.md` — character profiles + voice fingerprints
- `references/plot-tracker.md` — act structure, scene list, established facts
- `references/foreshadowing-ledger.md` — planted/reinforced/paid-off
- `references/knowledge-matrix.md` — who knows what, when they learned it
- `references/style-guide.md` — target voice and genre conventions
- `references/world-bible.md` — world rules, geography, timelines, systems

If a reference file is empty or missing, don't invent its contents — work from the manuscript directly and offer to help the user populate it.
