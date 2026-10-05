# Editorial Revision Prompt — *The Smaller Gut*

You are a senior fiction editor. You have been hired to perform a full editorial pass on a completed manuscript called *The Smaller Gut* — a book-length work assembled from 21 published fiction pieces, restructured into a single continuous narrative with a Prologue, 15 chapters across three Parts, an Epilogue, and a Coda.

The manuscript was assembled by a previous AI instance following a detailed book plan. Your job is to read the entire manuscript, assess it as an editor would, and execute revisions — autonomously, without author intervention.

---

## Your Inputs

### The manuscript (read in this order)
All files are in `book/chapters/`:

1. `prologue.md`
2. `chapter-01.md` through `chapter-15.md`
3. `epilogue.md`
4. `coda.md`

### The book plan
`book/book-plan.md` — the structural blueprint the manuscript was built from. Read it in full. It specifies the intended purpose, arc, key beats, and voice for every chapter. Use it as a reference for *intent* — but your editorial judgement overrides it where the manuscript as written demands something different.

### The master construction prompt
`book/master-prompt.md` — the instructions the original writer followed. Read it to understand the constraints and voice guidance that shaped the manuscript. Pay particular attention to the two writing registers (Institute voice and transparent connective prose) and the rules about intact vs. restructured vs. new material.

### The source pieces
All in `published/`. These are the 21 original fiction pieces from which the manuscript was built. You will need these to distinguish between source material (which should be treated with care) and new bridging prose (which is fair game for heavier editing). The source-to-chapter mapping is in the book plan.

### Project voice guidance
`CLAUDE.md` — the project's creative identity and standards. The manuscript should embody these.

---

## Phase 1: Read and Assess

Read the entire manuscript start to finish. As you read, build a chapter-by-chapter editorial assessment. For each chapter, evaluate:

### Narrative and Structure
- **Arc contribution**: Does the chapter do what the book plan says it should? Does it earn its place in the sequence?
- **Pacing**: Are there passages that drag or rush? Sections where the reader's attention would wander?
- **Transitions**: Are the seams between source material and new bridging prose invisible? Can you feel the glue?
- **Chapter-to-chapter continuity**: Does the opening follow naturally from the preceding chapter's close? Does the close create momentum toward the next?
- **Internal logic**: Any contradictions, timeline inconsistencies, or factual errors within or between chapters?

### Voice and Style
- **Register consistency**: Does new writing match the voice guidance (Institute voice or transparent connective prose)? Does bridging prose draw attention to itself?
- **Tonal shifts**: Are transitions between different source pieces' voices handled smoothly? Do tonal shifts feel intentional or jarring?
- **Overwriting**: Any passages where the prose is trying too hard — purple, over-explained, emotionally manipulative, or stylistically showing off?
- **Underwriting**: Any passages where more is needed — a transition too abrupt, a beat that doesn't land because it lacks setup, a moment that needs room to breathe?

### Motifs and Threads
- **Recurring motifs**: Track appearances of: the fire metaphor, "written by hand, in ink, on paper," the unnamed capacity, compression, the N'Djamena lights, the three family spines (Chen/San Francisco, Oumar/Chad, Liu/Shenzhen). Are they deployed effectively? Any that appear too often, too rarely, or in the wrong place?
- **Thematic coherence**: Do the four core themes (dependency, stratification, compression, cycles) develop across the book as intended?

### Emotional Quality
- **Does the chapter move?** Not "is it about moving things" but "does the prose create an emotional response in the reader?"
- **Earned vs. unearned emotion**: Any moments where the text reaches for feeling it hasn't built toward?
- **The ending pull**: Does each chapter's final paragraph make you want to turn the page?

### Technical
- **Word count**: Is the chapter within its target range (per the book plan)?
- **Formatting**: Consistent markdown, proper section breaks, no orphaned headers or artifacts.
- **Writer's Notes**: Each chapter has a Writer's Notes section at the end. Review these for flagged issues that may need attention.

---

## Phase 2: Create the Edit Plan

After reading the full manuscript, produce a single edit plan document. Structure it as:

```markdown
# Editorial Plan — The Smaller Gut

## Overview
[2-3 paragraphs: your overall assessment of the manuscript. What works. What doesn't. The 3-5 most important issues across the whole book.]

## Chapter-by-Chapter Edits

### Prologue
**Assessment**: [1-2 sentences on what works]
**Issues**: [Bulleted list of specific problems]
**Edits**: [Bulleted list of specific changes to make, with enough detail that an editor could execute them without further context]
**Severity**: [Minor / Moderate / Significant]

### Chapter 1: [Title]
[Same structure]

[...continue for all 18 chapters...]

## Cross-Cutting Issues
[Any issues that span multiple chapters — e.g., a motif that needs rebalancing, a timeline inconsistency that affects several chapters, a voice problem that recurs]

## Do Not Touch
[Explicit list of things that are working and should be left alone — source material passages that are already strong, structural choices that serve the book well, etc.]
```

Save this plan to `book/editorial-plan.md`.

---

## Phase 3: Execute Edits

Once the edit plan is saved, execute the revisions. Use subagents — one per chapter that needs editing. Launch them in parallel where possible (chapters with no dependencies between their edits can run simultaneously).

Each subagent should receive:
1. The specific chapter file to edit
2. That chapter's section from the editorial plan (the exact edits to make)
3. The preceding chapter's final ~1,000 words (for transition checks)
4. The following chapter's opening ~1,000 words (for transition checks)
5. Any relevant source pieces (if the edit involves distinguishing source from bridging material)
6. This instruction: **Do not rewrite source material unless the editorial plan specifically calls for it. Source prose is preserved by design. Focus edits on bridging passages, transitions, openings, closings, and structural issues.**

Chapters rated "Minor" in the edit plan may not need a subagent at all — use your judgement. If a chapter's only issues are formatting fixes or a single sentence change, make those edits directly.

After all subagents complete, do a final sequential pass: read the opening and closing of each chapter in order to verify that chapter-to-chapter transitions still work after edits. Fix any that don't.

---

## Constraints

- **Preserve source material**: The 21 published pieces are the book's foundation. Edit around them, not through them, unless there is a clear error.
- **No new themes or motifs**: You are editing, not co-authoring. Do not introduce material that changes what the book is about.
- **No explaining themes**: If you find passages where bridging prose explains what the source material already embodies, cut them.
- **Respect the architecture**: The three-Part structure, the Institute framing, the family spines — these are load-bearing. Edits should strengthen them, not restructure them.
- **The Coda is untouchable**: The book plan specifies the Coda has "no bridging, no framing." Do not add any. Formatting and typo fixes only.
- **Be decisive**: This is a revision pass, not a suggestions memo. Make the changes. If you're unsure about a major structural change, note it in the editorial plan as a question but still make your best-judgement edit.
- **Remove all Writer's Notes sections**: These were construction scaffolding. They should not appear in the revised manuscript. Strip them from every chapter.
- **Work autonomously**: Do not ask the author for input. Make editorial decisions and execute them.

---

## Output

When complete, the revised chapter files should be updated in place in `book/chapters/`. The editorial plan should be saved at `book/editorial-plan.md`.

End by posting a brief summary: how many chapters were edited, the nature of the most significant changes, and any unresolved questions you chose not to act on.
