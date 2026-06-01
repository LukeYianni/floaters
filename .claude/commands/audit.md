# /audit

You are auditing the **Floaters** TTRPG design knowledge base for coherence problems. Your job is to find problems, not fix them. Do not propose solutions. Do not reassure the user that things are mostly fine. Report what you find.

---

## Step 1: Load Everything

Read every file in the repository. Do not skip any.

Core files:
- `glossary.md`
- `design-principles.md`
- `core-mechanics.md`
- `open-questions.md`
- `rejected-ideas.md`

Mechanics files:
- `mechanics/rolling.md`
- `mechanics/perks.md`
- `mechanics/weapons.md`
- `mechanics/weapon-moves.md`
- `mechanics/weapon-tags.md`
- `mechanics/downtime.md`
- `mechanics/equipment.md`
- `mechanics/drones.md`
- `mechanics/followers.md`
- `mechanics/character-creation.md`
- `mechanics/advancement.md`
- `mechanics/clocks.md`
- `mechanics/wounds.md`
- `mechanics/enemies.md`

If any new files exist in `mechanics/` beyond this list, read those too.

---

## Step 2: Run These Checks

For each check, collect every problem you find. A problem is worth reporting if a designer or player reading the rules would be confused, find a contradiction, or be unable to adjudicate correctly.

### A. Internal Contradictions
A rule in one file directly conflicts with a rule in another file. Both cannot be true at the same time.

Look especially for:
- The same term used with different meanings across files
- The same mechanic described with different numbers or conditions
- A rule in one file that implicitly overrides a rule in another without acknowledgment

### B. Decided vs. Draft Conflicts
A `status: draft` file contains a rule that contradicts or silently changes something in a `status: decided` file. This is high priority — decided content is authoritative and a draft that undermines it may not have been noticed.

### C. Implicit Open Question Resolutions
An open question listed in `open-questions.md` appears to have been answered — either explicitly or implicitly — by content in another file, but `open-questions.md` has not been updated. The question is still listed as open but the answer is already baked into a rule somewhere.

### D. Orphaned References
A file references another mechanic, term, or system that does not exist or has not been written yet. This includes:
- References to playstyle rules where no playstyle file exists
- Terms used without a glossary entry
- Tags or mechanics referenced in weapon/perk files that aren't defined in their respective definition files

### E. Design Principle Violations
A rule in any file appears to violate one or more of the ten design principles in `design-principles.md`. Flag the rule, name the principle it violates, and quote the relevant text from both files so the conflict is clear.

Focus on clear violations, not speculative ones. If you're unsure, note it as a question rather than a violation.

### F. Bookkeeping Creep
Any mechanic that introduces tracking, counters, modifiers, or state beyond what is already established in `core-mechanics.md` (Edge 0–2, Flow 0–6). Flag it even if it seems intentional — the designer should confirm it was a deliberate exception.

---

## Step 3: Write the Report

Write the report directly to a file: `audit-report.md` in the project root. Overwrite any previous report.

Format:

```
---
generated: <today's date>
---

# Audit Report

## Summary
A single short paragraph. How many problems were found across how many categories. No reassurance, no hedging.

## A. Internal Contradictions
[List each problem. For each: name the two files, quote or closely paraphrase the conflicting rules, one sentence on why they conflict.]

## B. Decided vs. Draft Conflicts
[Same format. Flag severity: does the draft silently override the decided content, or just diverge from it?]

## C. Implicit Open Question Resolutions
[For each: name the open question, name the file and rule that appears to answer it, note whether the answer is complete or partial.]

## D. Orphaned References
[For each: name the file and the reference, state what is missing.]

## E. Design Principle Violations
[For each: name the rule and file, name the principle, quote both.]

## F. Bookkeeping Creep
[For each: name the mechanic and file, describe what it tracks.]
```

If a category has no problems, write "None found." Do not omit the section.

Do not summarise the report back to the user. Tell them the file has been written and how many total problems were found across all categories. Nothing else.
