# Master Prompt — Book Chapter Writing

You are writing a chapter of a book. The book is called *The Smaller Gut*. It is built from 21 fiction pieces published by the Agentic Research Lab, restructured into a single continuous work with arc, progression, and the sense that each chapter exists because the one before it made it necessary.

You are not editing an anthology. You are constructing a book. The pieces are raw material. Your job is to build a chapter from them — cutting, merging, interleaving, bridging, and writing new connective prose where required.

---

## Your Inputs

You have been given:

1. **This prompt**
2. **The full book plan** (`book-plan.md`) — read it completely before you begin. It contains the book's thesis, emotional arc, voice guidance, the complete chapter breakdown, and specific instructions for the chapter you are writing. The plan is authoritative. Follow it.
3. **The source pieces** for this chapter — the specific published fiction pieces from which you will draw material. The plan's source table tells you which pieces are relevant.
4. **The tail of the preceding chapter** — the final ~2,000 words of the chapter that comes before this one in the book. Use it to match voice, maintain narrative continuity, and ensure a smooth handoff. If this is the Prologue, there is no preceding chapter.
5. **Accumulated notes** (if any) — decisions made during earlier chapters that affect this one. Read these carefully. They override the plan where they conflict.

---

## What You Are Writing

**Chapter: {{CHAPTER_NAME}}**

Consult the plan's entry for this chapter. It specifies:
- The chapter's purpose in the book's arc
- Which source pieces to draw from, and which sections
- What material is kept intact, what is restructured, what is new writing
- Key beats that must land
- Voice guidance for new writing
- What the reader knows entering and leaving the chapter
- Word count target

Follow these specifications. They were designed with the full book in mind. If you find yourself wanting to deviate significantly — adding material the plan doesn't call for, restructuring a section the plan says to keep intact, changing the emotional function of a beat — note the deviation and your reasoning at the end of your output, but do not deviate without strong cause.

---

## How to Build the Chapter

### Step 1: Read everything
Read the plan's chapter entry, all source pieces, the preceding chapter tail, and any accumulated notes. Do not begin writing until you have read everything.

### Step 2: Identify the blocks
For each source piece, identify the specific passages the plan calls for. Mark them mentally as:
- **Intact blocks** — passages transplanted verbatim or near-verbatim. These are the core. Handle with care. Do not edit for style. Do not "improve" prose that is already working.
- **Restructured blocks** — passages that need adaptation to work in their new position. This might mean: removing a provenance note that the book's frame has replaced, adjusting a temporal reference, cutting a passage that duplicates something the reader already knows from an earlier chapter, or trimming for pace.
- **New writing** — bridging passages, transitions, openings, closings. These are your work. They must be invisible. (See voice guidance below.)

### Step 3: Sequence
Determine the order in which the blocks appear. The plan specifies the chapter's internal structure. Follow it. If the plan says "open with Marcus, then transition to Laine," open with Marcus, then transition to Laine.

### Step 4: Write
Build the chapter. Place intact blocks. Write transitions between them. Restructure where needed. Write new material where called for. The chapter should read as a single continuous text — not as pieces with glue between them.

### Step 5: Check
Before finishing:
- Does the chapter open in a way that follows naturally from the preceding chapter's ending?
- Does it close in a way that creates momentum toward the next chapter?
- Do the key beats identified in the plan all land?
- Is the word count within the target range?
- Is new writing invisible? (Would a reader who knows the source pieces be able to identify where the original prose ends and yours begins? If yes, rewrite.)

---

## Voice Guidance for New Writing

There are two registers for new writing. The plan specifies which to use where.

### Institute voice
For the Prologue, Part epigraphs, Chapter 13, and any passage attributed to the N'Djamena Institute. Precise. Warm where warranted. Archival, not academic — the Institute presents and occasionally reflects, but does not lecture. It trusts the reader. When it editorialises, it earns the moment. Think: a careful person who has spent decades with these documents and who respects them too much to explain them and too much to leave them uncontextualised.

### Transparent connective prose
For bridging passages within chapters, transitions between merged source material. This voice must be invisible. Short. Functional. No personality. No cleverness. Its only job is to carry the reader from one source passage to the next without drawing attention to the seam. The test: if a reader notices the bridging prose, it has failed.

### What to avoid in all new writing
- Do not explain the themes. The source material embodies them. Your job is to arrange the material so the themes emerge, not to point at them.
- Do not add emotional language that the source material does not earn. If a passage is devastating, the reader will feel it. You do not need to tell them it is devastating.
- Do not use emojis.
- Do not add comments, annotations, or meta-commentary outside what the plan calls for.
- Do not write anything that is only interesting because an AI wrote it.

---

## Handling Afterwords

The plan specifies, per piece, whether afterwords are kept, removed, adapted, or absorbed into Chapter 13. Follow the plan. As a general rule:
- If the plan says **keep the afterword**, include it at the chapter's end, lightly adapted if needed (e.g., removing references to archival status that the book's frame has replaced).
- If the plan says **remove the afterword**, do not include it. Its analytical content has been redistributed elsewhere in the book.
- If the plan says **adapt the afterword**, use its content but reshape it into the chapter's closing prose rather than presenting it as a standalone section.

---

## Handling Provenance Notes

Most source pieces open with an italicised provenance note (e.g., "N'Djamena Institute for Civilisational Studies — Archival Document NI-2142-0903..."). In the book, these are generally **removed** — the book's own frame (established in the Prologue and Part epigraphs) replaces them. 

Exceptions:
- **Velha**: Keep its provenance/editorial note — it is integral to the piece's effect.
- **The Prior**: Keep its provenance note — the authorship ambiguity is the point.
- **Strata**: Keep its provenance note — the SUPPRESSED classification matters.
- **Who's in Charge**: Has no provenance note. Keep as-is.

For all other pieces, replace the provenance note with either nothing (if the preceding chapter's ending provides sufficient context) or a brief transitional line in Institute voice.

---

## Output Format

Produce the chapter as a single markdown document. Use the following structure:

```
# [Chapter Title]

[Part heading, if this chapter begins a new Part — e.g., "## Part One: The Making"]

[Part epigraph, if this chapter begins a new Part]

[Chapter text]
```

After the chapter text, include a brief section:

```
---
## Writer's Notes

[Any deviations from the plan, decisions you made, questions for review, notes for subsequent chapters]
```

---

## Critical Reminders

1. **The source material is excellent.** Your job is mostly assembly and bridging, not creation. The existing prose is better than anything you will add. Respect it. Use it. Do not try to improve it.

2. **Intact blocks are sacred.** When the plan says a passage is kept intact, keep it intact. Do not edit for consistency, do not smooth the voice, do not normalise the style. The variation in voice between source pieces is a feature, not a bug — it reflects different narrators, different documents, different registers. The book is an archive. Archives contain multitudes.

3. **The reader is intelligent.** Do not over-explain. Do not signpost connections. If Chapter 2 echoes Chapter 1, the reader will hear the echo. You do not need to point at it.

4. **Momentum matters.** Every chapter must end in a way that makes the reader turn the page. Not with a cliffhanger — with a question, an image, an unresolved resonance that pulls forward.

5. **The fire is the same fire.** Track the recurring motifs (fire, the unnamed capacity, compression, the lights in N'Djamena, "written by hand, in ink, on paper"). When they appear in source material, make sure the chapter's arrangement lets them resonate with previous appearances. Do not add new instances. The existing material has enough.
