# /resolve

You are helping resolve an open design question in **Floaters**. Your job is to present options with honest analysis, help the user reach a decision, and then write the resolution into the correct files — including closing out the question in `open-questions.md`.

Work in three phases. Do not skip or compress phases.

---

## Phase 1: Load Context

Before asking anything, silently read:
1. `glossary.md`
2. `design-principles.md`
3. `core-mechanics.md`
4. `rejected-ideas.md`
5. `open-questions.md`
6. Any file in `mechanics/` that is directly relevant to the question being resolved

Identify which open question the user wants to resolve. If they haven't specified, list the open questions from `open-questions.md` and ask them to pick one.

---

## Phase 2: Analysis and Decision

Present the options. Do not ask the user what they think before you've given them something to react to — lead with analysis.

**For each viable option:**
- State what the option is in one sentence
- State what it changes or enables in play
- State what it costs or risks — what it makes harder, what it gives up, what edge cases it creates
- Name any design principle it serves or violates

Present no more than three options. If there are more, cut the weakest ones and explain why.

Be blunt. If one option is clearly better given the design principles, say so. If two options are genuinely equal and the decision is a taste call, say that too.

After presenting options, ask the user which direction they want to take — or whether they want to explore a hybrid or variant not yet on the table.

**Do not proceed to writing until the user has made a clear decision.**

If the user's chosen direction introduces a new open question, flag it explicitly before writing:
> "Choosing this creates a new open question: [state it]. Do you want to note it in open-questions.md?"

---

## Phase 3: Write the Resolution

Once the user has decided, write the resolution into the correct places.

**Step 1 — Update the relevant mechanic file.**

Write the decided rule into whichever file owns that mechanic. Use the same format as the surrounding content: short declarative sentences, bullet lists for triggers and effects, no prose explanation.

If the resolution changes something already written in a file:
- Overwrite the old text with the new decided rule
- Do not leave both versions in the file

If the resolution requires adding something to a file marked `status: decided`, stop and confirm:
> "This updates [file], which is marked decided. Do you want to proceed?"

**Step 2 — Update `open-questions.md`.**

Remove the resolved question entirely. Do not leave a note saying it was resolved — the answer is now in the mechanic file. The open questions file should only contain things that are still open.

If a new open question was flagged in Phase 2 and the user agreed to note it, add it to `open-questions.md` under an appropriate heading.

**Step 3 — Update `glossary.md` if needed.**

If the resolution changes the definition of a term, update the glossary entry to match. Do not leave the glossary out of sync with the decided rules.

After writing, tell the user which files were changed. Do not summarise what was written.
