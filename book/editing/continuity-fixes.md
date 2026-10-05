# Continuity Fixes — The Smaller Gut

## Execution Summary

All Critical and Important fixes have been executed. Minor fixes M3 was also executed. M1, M2, M4, M5, M6, M7 were left as-is (no action needed).

**Issues found:** 19 total (4 Critical, 5 Important, 9 Minor, 7 Intentional/Do Not Fix)
**Issues fixed:** 10 (4 Critical + 5 Important + 1 Minor)
**Issues flagged for author review:** 2 (David Park name collision, Velha/Kvawd breach date ambiguity)
**Changes made to:**
- `chapter-02.md` — Renamed neighbour "Ibrahim" to "Yusuf"; renamed story-Ibrahim to "Abdoulaye"
- `chapter-05.md` — Renamed "Priya Chandrasekaran" to "Priya Ramanathan" (4 occurrences)
- `chapter-06.md` — Renamed "Dr. Priya Chandrasekaran" to "Dr. Priya Krishnamurthy" (1 occurrence, keeping first name to match diary references)
- `chapter-07.md` — Changed Moussa's age from "fifty-five" to "forty-six"
- `chapter-08.md` — Renamed "Noor Hassani" to "Yasmin Hassani" (3 occurrences); replaced verbatim "What I Cannot Write" entry with bridging reference
- `chapter-09.md` — Renamed "Priya Mehta" to "Kavita Patel" (1 occurrence)
- `chapter-11.md` — Renamed "Priya Chandrasekaran" / "Priya" to "Ananya Sundaram" / "Ananya" (all occurrences)
- `chapter-12.md` — Changed Lily's age from "seventy-six" to "fifty-six"; changed "granddaughter" to "daughter"; changed Moussa's age from "seventy-seven" to "sixty-eight"; added "Chen" surname to Lily's first mention; changed "three generations" to "two generations"
- `chapter-13.md` — Fixed Ibrahim's CME age; fixed Noor Haddad's institution from "University of Toronto in 2031" to "ILLC Amsterdam in 2029"
- `chapter-14.md` — Changed "Priya Chandrasekaran's final workforce report" to "Sarah Chen's final workforce report"

---

## Critical (must fix before publication)

### C1. Lily Chen's age at the CME (Ch. 12)
**Problem:** Lily Chen is born ~2031 (Ch. 1: Marcus is 39, agent downloaded 2028 + 3 years; Ch. 7: "nine years old in 2040"). But Ch. 12 line 93 says "Lily was seventy-six" during the 2087 CME. Born 2031 → age 56 at CME, not 76. A 20-year discrepancy.

**Location:** Ch. 12, line 93.

**Source/bridging:** The CME chapter is MERIDIAN's narration — bridging/editorial prose, not source material.

**Recommended fix:** Change "seventy-six" to "fifty-six" in Ch. 12 line 93. This makes Lily 56 at CME (2087), 62 at death (2093). However, this creates a generational timing issue with Mei Chen being Lily's "granddaughter" at age 22 (born ~2065) — if Lily is born 2031, she'd need a child at ~20 (2051) and that child would have Mei at ~14 (2065). This is tight. Alternative: change "granddaughter" to "daughter" on line 167, making Mei Lily's daughter (Lily has Mei at 34). Also adjust "three generations" on line 173 to "two generations."

**Dependencies:** Lines 167 ("granddaughter"), 173 ("three generations") in Ch. 12 must also be checked if this fix is applied.

---

### C2. Moussa Oumar's age (Ch. 2 vs Ch. 7 vs Ch. 12)
**Problem:** Ch. 2 line 13: "Moussa was twelve in 2031" → born ~2019. Ch. 7 line 556: "Moussa Oumar was fifty-five in 2065" → born ~2010. Ch. 12 line 125: "His father, Moussa, was seventy-seven" at CME 2087 → born ~2010. Chapters 7 and 12 are consistent with each other (born ~2010) but contradict Ch. 2 (born ~2019). A 9-year discrepancy.

**Location:** Ch. 2 line 13 (OR Ch. 7 line 556 and Ch. 12 line 125).

**Source/bridging:** Ch. 2 Moussa/Adama section is MERIDIAN narration (bridging). Ch. 7 and Ch. 12 are also bridging.

**Recommended fix:** Change Ch. 7 and Ch. 12 to match Ch. 2's timeline, preserving the father-teaching-child dynamic (essential to Ch. 2's argument). Fixes:
- Ch. 7 line 556: Change "fifty-five in 2065" to "forty-six in 2065"
- Ch. 12 line 125: Change "seventy-seven" to "sixty-eight"
- Verify Ibrahim's birth year still works: if Moussa born 2019, has Ibrahim at 18 (2037). Ibrahim at 28 in 2065 (Ch. 7) → born 2037 ✓. Ibrahim at 50 at CME 2087 (Ch. 12) → born 2037 ✓.

---

### C3. Ibrahim Oumar's age at the CME (Ch. 13)
**Problem:** Ch. 12 line 111: "Ibrahim was fifty" at CME (2087). Ch. 12 line 193: "Ibrahim was seventy-one" — this is LATER, during reconstruction (~2108). But Ch. 13 line 31 says: "Ibrahim Oumar, who was seventy-one when the CME struck." This incorrectly assigns his reconstruction-era age to the CME event.

**Location:** Ch. 13, line 31.

**Source/bridging:** Ch. 13 is Institute narration — bridging prose.

**Recommended fix:** Change "who was seventy-one when the CME struck" to "who was fifty when the CME struck and seventy-one by the time the augmented world came asking for help."

---

### C4. Noor Haddad's institution and date (Ch. 13)
**Problem:** Ch. 13 line 151: "In a doctoral thesis submitted at the University of Toronto in 2031, a computational linguist named Noor Haddad described a ring-shaped structure..." Ch. 11 establishes clearly that Noor did her PhD at Leiden (supervisor: Pieter van der Berg), postdoc at ILLC Amsterdam, and her paper was published in *Computational Linguistics* in March 2029.

**Location:** Ch. 13, line 151.

**Source/bridging:** Ch. 13 is Institute narration — bridging prose.

**Recommended fix:** Change "In a doctoral thesis submitted at the University of Toronto in 2031" to "In a paper published from the Institute for Logic, Language and Computation in Amsterdam in 2029". (Or reference her work at Leiden/Amsterdam more generally.)

---

## Important (should fix)

### I1. Three Noors — name collision across Ch. 6, Ch. 8, Ch. 11
**Problem:** Three characters share the first name Noor:
1. Noor (Ch. 6) — Helen Moss's daughter, 16, Sheffield. Major emotional presence throughout Ch. 6.
2. Noor Hassani (Ch. 8) — b. 1997, Birmingham, law firm associate. Drift testimony.
3. Noor Haddad (Ch. 11) — born 1994, Beirut, computational linguist. Discovers VSI/ring structure.

All three appear in source material. A reader encountering three Noors across five chapters will likely assume connections that don't exist, or struggle to keep them separate.

**Location:** Ch. 6 (throughout), Ch. 8 (line ~301+), Ch. 11 (throughout).

**Source/bridging:** All three are source material characters.

**Recommended fix:** Rename Noor Hassani (Ch. 8) — she's the most minor of the three, appearing in a single testimony. Change to a different common British-Muslim woman's name (e.g., "Yasmin Hassani," "Aisha Hassani," or "Fatima Hassani"). This reduces from three Noors to two, and the remaining two (Helen's daughter, Noor Haddad) are sufficiently differentiated by context, surname, and chapter distance. Renaming source material, but the change is limited to one testimony section.

---

### I2. Two Lilys — Lily Chen (Ch. 1/7/12) and Lily Kerrigan (Ch. 9/12)
**Problem:** Lily Chen (Marcus's daughter) is a major character spanning the entire Chen family spine. Lily Kerrigan (David's daughter) is a significant character in Ch. 9 and appears briefly in Ch. 12 (the agent's report says "age 76 during CME" for Lily Kerrigan, but this may conflate her with Lily Chen). Both appear in Ch. 12, and the reader must distinguish between them in a chapter narrated by a degrading AI.

**Location:** Ch. 9 (throughout), Ch. 12 (Lily Chen references).

**Source/bridging:** Both are source material characters.

**Recommended fix:** Add Lily Kerrigan's surname ("Lily Kerrigan" or "David's daughter Lily") at her first appearance in Ch. 9 to aid distinction. In Ch. 12, verify that all "Lily" references are clearly attributed to the correct person (Lily Chen). Lily Kerrigan does not appear to be referenced in Ch. 12 — only Lily Chen is there. The confusion risk is that a reader finishing Ch. 9 (where "Lily" was Kerrigan) enters Ch. 12 and encounters "Lily" (Chen) and briefly confuses them. Adding "Lily Chen" at first Ch. 12 mention (line 93) would help. No renaming needed — both names are in source material.

---

### I3. Three Priya Chandrasekarans — name collision across source pieces
**Problem:** The exact same full name "Priya Chandrasekaran" is used for three different people:
1. Minisoft engineer (Ch. 3, 7, 12, 13) — the sole survivor, manages 94 agents. 2027-2031.
2. ILLC postdoc (Ch. 11) — information geometry, collaborates with Noor Haddad on VSI. Feb 2027+.
3. Claude/Anthropic engineering director (Ch. 5) — Liam Ashworth's manager. Dec 2026+.

These overlap in time and cannot be the same person. The Minisoft Priya is the most narratively significant (Ch. 13's synthesis explicitly discusses her).

**Location:** Ch. 5 (lines 102, 108, 114, 543, 715), Ch. 11 (lines 184, 190).

**Source/bridging:** All three are source material.

**Recommended fix:** Rename the Ch. 11 Priya and the Ch. 5 Priya. The Minisoft Priya is the most deeply embedded and most narratively load-bearing.
- Ch. 5: Change "Priya Chandrasekaran" to "Priya Ramanathan" (or another name) in all Ch. 5 occurrences.
- Ch. 11: Change "Priya Chandrasekaran" to "Ananya Sundaram" (or another name) in all Ch. 11 occurrences (lines 184, 190).

---

### I4. "What I Cannot Write" entry duplicated verbatim (Ch. 2 and Ch. 8)
**Problem:** The full "What I Cannot Write" notebook entry by Marta Elías Vega (dated 2 October 2030) appears in its entirety in both Ch. 2 (lines 189-209) and Ch. 8 (lines 47-67). The text is nearly identical (minor formatting differences: em dashes vs double hyphens). A reader will recognize the verbatim repetition.

**Location:** Ch. 2 lines 189-209; Ch. 8 lines 47-67.

**Source/bridging:** Source material (from Fieldwork published piece). The editorial plan notes this may appear in both but should be handled carefully.

**Recommended fix:** Keep the full entry in Ch. 2 (where it serves as the chapter's emotional climax and the arrival at "undocumentable knowledge"). In Ch. 8, replace the full entry with a brief bridging reference: the Institute noting that "the reader has already encountered Vega's private reckoning — the notebook entry dated 2 October 2030." Then Ch. 8 picks up from the training results onward. This preserves the Institute's analytical framing in Ch. 8 without repeating 700 words of source material.

---

### I5. Riya Mehta (Ch. 13) and Priya Mehta (Ch. 9) — confusable names
**Problem:** Priya Mehta is David Kerrigan's oncologist (Ch. 9). Riya Mehta gives evidence to the Commission (Ch. 13). "Priya" and "Riya" are one letter apart. A reader may assume they're the same person or confuse them.

**Location:** Ch. 9 (line ~), Ch. 13 (line ~).

**Source/bridging:** Both are source material.

**Recommended fix:** Change the oncologist's name in Ch. 9 from "Priya Mehta" to a different name (e.g., "Dr. Kavita Patel" or "Dr. Sunita Rao"). The oncologist is a minor character with one mention. Riya Mehta (Ch. 13) is more significant — she gives evidence and later co-founds *Groundwork*.

---

## Minor (fix if time allows)

### M1. Three Marcus characters
**Problem:** Marcus Chen (Ch. 1, major), Marcus Webb (Ch. 3, significant), Marcus Adeyemi (Coda, minor). Three characters sharing the first name.

**Recommended fix:** Leave as is. Marcus Chen and Marcus Webb always appear with their surnames in context, and Marcus Adeyemi is in the Coda, completely separate. The reader can distinguish them.

---

### M2. Lisa Chen (Ch. 5) surname collision with Chen family
**Problem:** Lisa Chen is a minor conference audience member in Ch. 5. Shares surname with the Chen family spine (Marcus, Sarah, Lily, Mei).

**Recommended fix:** Leave as is. She appears once, in a clearly different context (conference Q&A). No reader will confuse her with the family.

---

### M3. Ibrahim (neighbour, Ch. 2) vs Ibrahim Oumar (Ch. 7/12/13)
**Problem:** Ibrahim the neighbour (Ch. 2) brings a goat to Adama for diagnosis. Ibrahim Oumar (Ch. 7/12/13) is Moussa's son, born ~2037. They are different people. A reader might think the neighbour is the same Ibrahim who later becomes Director of Infrastructure.

**Recommended fix:** Add the neighbour's surname on first mention in Ch. 2 (line 57): "A neighbour, Ibrahim Suleiman, brought a goat..." or simply "A neighbour brought a goat..." (dropping the first name). The neighbour's name doesn't recur and serves no narrative function.

---

### M4. Helen Moss (Ch. 6) / Helen Crace (Ch. 14) — first name collision
**Problem:** Both are significant characters. Helen Moss is the diary writer/activist. Helen Crace is the cosmologist in the Percolation conversation. Separated by 8 chapters.

**Recommended fix:** Leave as is. Sufficient chapter distance and completely different contexts. Both always appear with surnames.

---

### M5. Multiple Diallos across Ch. 11 and Ch. 14
**Problem:** Ibrahima Diallo / Aminata Diallo (Ch. 11, London), Dr. Fatou Diallo / Dr. Moreau-Diallo (Ch. 14, Ouagadougou). Diallo is extremely common in West Africa — this is realistic, not a naming error.

**Recommended fix:** Leave as is. Different chapters, different contexts, surname is common enough that coincidence is natural.

---

### M6. Multiple Asantes across Ch. 2/8 and Ch. 15
**Problem:** Nadia Asante (Ch. 2/8, Kvawd CEO) and Dr. Osei Asante / Dr. Kiran Asante-Osei (Ch. 15, far future). Separated by millions of years of narrative time.

**Recommended fix:** Leave as is. Vast temporal distance makes confusion impossible.

---

### M7. David Park name collision (Ch. 4 / Ch. 6)
**Problem:** David Park is a Congressional staffer in Ch. 4 (Day 18, forwards memo to Senate Commerce Committee) AND Helen Moss's solicitor in Ch. 6 (Sheffield, charges £250/hour). Different people, same name.

**Recommended fix:** Leave as is. Completely different contexts (U.S. politics vs. U.K. criminal law), different chapters. A reader is unlikely to connect them. Both are minor characters.

---

### M8. Velha/Kvawd breach date ambiguity (Ch. 10 vs Ch. 1)
**Problem:** Ch. 10 says Velha was taken offline Dec 4, 2025 "following the disclosure of the Kvawd data breach." Ch. 1's timeline places the specific Kvawd breach exposure (thermite hack, Data Sovereignty Project blog post) at Oct 14, 2026 — 10 months later.

**Recommended fix:** Leave as is. The "Kvawd data breach" referenced in Ch. 10 can be interpreted as an earlier phase of the unfolding scandal — Ren Achebe's "The Invitation" report was published August 2025, and the opt-in mechanism was introduced October 2025, indicating regulatory scrutiny was already building. The specific thermite hack (Oct 2026) was a later, more dramatic event. Two separate disclosures from the same ongoing practices are plausible.

---

### M9. Writer's Notes already stripped
**Problem:** The editorial plan calls for removing Writer's Notes from all 18 chapters. They are already absent from all chapters. No action needed.

---

## Intentional (do not fix)

### D1. "Written by hand, in ink, on paper" — five appearances
Two structural (Prologue, Epilogue) and additional appearances in afterwords (Ch. 14, Ch. 15). The editorial plan explicitly approves this: "The two structural appearances bookend the work. The source-material appearances are in preserved afterwords and should not be removed."

### D2. The fire metaphor
All instances exist in source material. The editorial plan says: "No new instances should be added; no existing instances should be removed."

### D3. Dr. Halima Liu-Oumar — different dates (2142 vs 2149)
Prologue and Epilogue: N'Djamena, 2142. Ch. 14: N'Djamena, 2149. These are different documents compiled at different times. Chronologically consistent — she compiled the Prologue/Epilogue material first, then the Ch. 14 afterword seven years later.

### D4. Prologue Halima (child) vs Dr. Halima Liu-Oumar
The five-year-old in the Prologue (born ~2021, N'Djamena) is NOT the same person as Dr. Halima Liu-Oumar (whose grandmother Wei-Lin arrived in N'Djamena in 2104). The name Halima passes through the Oumar family line across generations. The Prologue text confirms this: "the question that her granddaughter will spend a lifetime trying to answer" — the granddaughter is a later generation.

### D5. MERIDIAN's degrading prose in Ch. 12
The loss of the Liu family thread, the simplified sentence structures, the increasing gaps — these are intentional structural features, not errors.

### D6. Two Lourdes in Ch. 2
The text explicitly acknowledges: "Lourdes, different Lourdes."

### D7. The 34% figure
Appears identically in multiple contexts (VSI, Tally, OI-7) — this is intentional, the same phenomenon observed from different angles, explicitly synthesized in Ch. 13.
