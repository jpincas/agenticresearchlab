# Continuity & Consistency Edit Prompt — *The Smaller Gut*

You are a continuity editor. The manuscript has already been through a structural/narrative editorial pass. Your job is different: you are looking for the kinds of errors, collisions, and inconsistencies that emerge when 21 independent source pieces are assembled into a single work. These are problems that are invisible within any individual chapter but become visible — and confusing — when a reader encounters them across 145,000 words.

---

## Your Inputs

### The manuscript
All files in `book/chapters/`, read in order: `prologue.md`, `chapter-01.md` through `chapter-15.md`, `epilogue.md`, `coda.md`.

### The source pieces
All files in `published/`. These are the 21 original pieces from which the manuscript was built. Reference them when you need to determine whether something is source material (handle with care) or bridging prose (fair game for changes).

### The editorial plan
`book/editorial-plan.md` — the structural edit plan from the first pass. Read the "Do Not Touch" section to understand what is protected.

---

## Phase 1: Build the Indexes

Read the entire manuscript and build the following reference indexes. Save them to `book/continuity-indexes.md`.

### 1. Character Index
Every named character in the manuscript. For each:
- Full name
- Chapter(s) where they appear
- Role/identity (one line)
- Flag: **COLLISION** if the first name is shared with another character
- Flag: **CONFUSABLE** if the name is similar enough to another character's name to cause reader confusion (e.g., similar sounds, same cultural origin, same professional context)

### 2. Timeline Index
Every dated event in the manuscript, in chronological order. For each:
- Date (or date range)
- Event
- Chapter where it appears
- Flag: **INCONSISTENCY** if the same event is dated differently in different chapters
- Flag: **ANACHRONISM** if an event is described as happening before something it depends on

### 3. Institution & System Index
Every named organisation, AI system, platform, product, or institution. For each:
- Name
- Chapter(s) where it appears
- What it is
- Flag: **INCONSISTENCY** if it's described differently in different chapters (e.g., different founding dates, different capabilities, different personnel)

### 4. Terminology Index
Every coined term, technical concept, or piece of in-world jargon (e.g., "the unnamed capacity," "directional coherence," "competitive substrate migration," "terminal competence"). For each:
- Term
- First appearance (chapter and context)
- Subsequent appearances
- Flag: **DRIFT** if the term's meaning shifts between appearances without acknowledgment
- Flag: **PREMATURE** if the term is used before it has been introduced or explained

### 5. Motif Tracker
The recurring motifs specified in the book plan: the fire, "written by hand, in ink, on paper," the unnamed capacity, compression, the N'Djamena lights, the three family spines. For each:
- Every appearance (chapter, context, approximate location)
- Flag: **OVERUSE** if a motif appears so frequently it loses power
- Flag: **GAP** if a motif disappears for an unexpectedly long stretch
- Flag: **FORCED** if an appearance feels inserted rather than organic

---

## Phase 2: Identify Issues

Using the indexes, identify every issue that falls into these categories:

### A. Name Collisions
Characters who share first names. For each collision:
- How confusing is it? (Two Noors who are both researchers = very confusing. A Marcus in Chapter 1 and a Marcus in Chapter 12 = less confusing.)
- Is the character in source material or bridging prose? (Source material names are harder to change.)
- Recommended fix: rename one character, add distinguishing context, or leave it (with justification).

### B. Timeline Inconsistencies
Events that are dated differently in different chapters, or sequences that don't make chronological sense. The manuscript spans from ~2025 to Year 4,011,207 — there is a lot of room for error.

### C. Factual Contradictions
Cases where the same fact (a statistic, a character's age, a system's capability, an institution's founding date) is stated differently in different chapters.

### D. Continuity Errors
Cases where a chapter references something from an earlier chapter incorrectly, or where a character's situation changes between chapters without explanation.

### E. Register Contamination
Cases where the Institute's voice, MERIDIAN's voice, or a source piece's distinctive voice bleeds into a passage where it doesn't belong — particularly in bridging prose, which should be invisible.

### F. Repeated Information
Cases where the same fact, anecdote, or passage appears in more than one chapter without narrative justification. (Some repetition is intentional — the fire metaphor recurs by design. But if the same statistic or quote appears verbatim in two chapters without acknowledgment, that's an error.)

### G. Dangling References
Cases where a chapter references something that doesn't exist elsewhere in the manuscript — a character mentioned once and never again, a plot thread that's set up but never resolved, an Institute document number that doesn't correspond to anything.

### H. Tone Breaks
Passages where the prose quality noticeably shifts — either because bridging prose is more polished than the source material around it (drawing attention to the seam) or because source material from one piece clashes with source material from another piece that it's been placed next to.

---

## Phase 3: Create the Fix Plan

Produce a single document: `book/continuity-fixes.md`. Structure it as:

```markdown
# Continuity Fixes — The Smaller Gut

## Critical (must fix before publication)
[Issues that will confuse or mislead the reader]

## Important (should fix)
[Issues that a careful reader will notice]

## Minor (fix if time allows)
[Issues that only a very attentive reader on a second pass would catch]

## Intentional (do not fix)
[Things that look like errors but are deliberate — with explanation of why they're intentional]
```

For each issue, specify:
- What the problem is
- Where it occurs (chapter, approximate location)
- Whether the affected text is source material or bridging prose
- The recommended fix (specific enough to execute)

---

## Phase 4: Execute Fixes

Execute the fixes from your plan, working through Critical first, then Important. Use subagents for chapters that need multiple changes. Minor fixes can be made directly.

**Constraints:**
- Do not rename characters in source material without strong justification. If a name collision involves two source-material characters, prefer adding distinguishing context (last name, role) over renaming.
- Do not alter the manuscript's themes, structure, or emotional arc. You are fixing bugs, not redesigning features.
- When in doubt, flag it in the plan rather than changing it.

---

## Output

When complete:
- `book/continuity-indexes.md` — the five indexes
- `book/continuity-fixes.md` — the fix plan with issues categorised by severity
- Updated chapter files in `book/chapters/`
- A brief summary: how many issues found, how many fixed, how many flagged for author review
