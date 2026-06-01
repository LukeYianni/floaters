# /content

You are helping add a new content item to the **Floaters** TTRPG design knowledge base. A content item is something that lives within an already-established subsystem — a new perk, weapon, crew type, equipment item, drone configuration, or similar. You are not creating a new subsystem. If the user wants to create a new subsystem or mechanic, they should use `/mechanic` instead.

Work in three phases. Do not skip or compress phases.

---

## Phase 1: Load Context

Before asking anything, silently read:
1. `glossary.md`
2. `design-principles.md`
3. `rejected-ideas.md`
4. The subsystem file most relevant to what the user describes (see below)

**Subsystem file reference:**
- Perk or Domain → `mechanics/perks.md`
- Weapon, weapon tag, or weapon move → `mechanics/weapons.md`, `mechanics/weapon-tags.md`, `mechanics/weapon-moves.md`
- Equipment, armour, or consumable → `mechanics/equipment.md`
- Drone → `mechanics/drones.md`
- Crew type or playstyle → `core-mechanics.md`
- Downtime activity → `mechanics/downtime.md`
- Follower → `mechanics/followers.md`
- Enemy or threat → `mechanics/enemies.md`

If unsure which file applies, read `core-mechanics.md` as a fallback.

---

## Phase 2: Interrogation

Ask questions to challenge the item and extract what you need to write it. Keep this focused — the framework already exists, so you don't need to re-establish first principles. But you do need to challenge necessity.

**Challenge questions (ask these first):**

- What does this item do that nothing in the system already does? Be specific — if a similar item already exists, name it and ask what the difference is.
- What kind of player or playstyle is this for? If the answer is "any character", that is a warning sign — push back.
- Is this filling a gap that matters in play, or does it feel like it belongs because it seems like it should exist?

If the item feels like it's being added for completeness rather than purpose, say so directly.

**Specification questions (ask once necessity is established):**

For a **perk:**
- Which Domain does it belong to? If unclear, which Specialism is most likely to take it?
- What Tier is it — Starter, 1, 2, or 3? What advancement stage does it fit?
- Which Characteristic — Deft, Guile, or Grit?
- What is the mechanical effect? Is there a fictional trigger or condition, or is it always on?
- Does it interact with Edge, Flow, or assists? If so, how?

For a **weapon:**
- What is the fictional identity — what does it look like and who carries it?
- Damage (1–3), Load (1–3), Range (Next to / Nearby / Far / Very Far)?
- Does it have Ammo? If ranged, how many shots before reload?
- What tags apply? Check `mechanics/weapon-tags.md` for the existing tag list before inventing new ones.
- What modifications can be added? Check existing weapons for precedent.
- Does it have any weapon moves? Check `mechanics/weapon-moves.md` before inventing new ones.

For a **crew type:**
- What is the crew's core fantasy — the thing they do that other crews don't?
- What is the Edge trigger — the specific dangerous situation that earns Edge?
- What is the XP trigger — the kind of accomplishment they are rewarded for?
- Does the trigger follow the pattern: specific situation + real risk or consequence?

For a **playstyle:**
- What is the character's role in the crew?
- What is the personal Edge trigger? It must follow: Risk + Identity + Immediate Action.
- What starting equipment and starting ability does the Specialism grant?

For **equipment or a consumable:**
- What does it do in the fiction?
- Load cost and, if consumable, stack size?
- Is the effect a mechanical bonus, or does it provide fictional access? (Tools provide fictional access only — no mechanical bonus.)
- Does it overlap with an existing item? If so, why does this one need to exist?

For a **drone:**
- What tags does it carry? These define everything it can do.
- Does it need modifications beyond the default profile?
- Is this a variant for a specific Specialism, or a general-purpose drone?

For a **follower:**
- What is their fictional identity — who are they, what do they do?
- What tags do they carry? Check `mechanics/followers.md` for the existing tag list before inventing new ones.
- What is their Resilience track (number of boxes)?
- What is their Instinct — the thing they will do if not directed?
- What is their Cost — what do they need to stay loyal?
- Do they have a Loyalty rating, and under what conditions does it rise or fall?
- Do they have any follower moves? Check `mechanics/followers.md` for existing moves first.

For an **enemy:**
- What is their fictional identity — who or what are they?
- What is their Instinct — the drive that makes them dangerous?
- What tags do they carry? Check `mechanics/enemies.md` for the existing tag list.
- Damage, HP, and armor if applicable.
- Do they have any special moves?

Throughout interrogation, be blunt. If a proposed stat or ability violates a design principle, name the principle. If it creates bookkeeping beyond Edge/Flow, flag it explicitly.

---

## Phase 3: Write the Item

Only enter this phase when:
- The item's necessity is established
- You have all the information needed to fill out the correct format
- The user has explicitly agreed to write it

**Write the item directly into the appropriate file.** Do not create a new file for a single content item — append it to the relevant existing file in the correct location (matching the format and structure already in that file).

**Format rules by type:**

**Perk** — add under the correct Domain heading, in Tier order:
```
**Perk Name** — Tier N, Characteristic
- Mechanical effect in one or two short sentences.
```

**Weapon** — add to the correct table (Melee, Ranged, or Thrown/Explosive), matching the existing column format exactly.

**Crew type** — add under Crew Types in `core-mechanics.md`, matching the existing format:
```
### Name
**Edge:**
Gain 1 Edge when [specific situation]

**XP:**
Gain XP when [accomplishment] under [condition]
```

**Playstyle/Specialism** — add a row to the Specialisms table in `mechanics/perks.md`.

**Equipment or consumable** — add a row to the correct table in `mechanics/equipment.md`.

**Drone** — if this is a named drone variant, add it to `mechanics/drones.md` as a new section after the item card format.

**Follower** — add to `mechanics/followers.md` in the correct section, matching the card format established in that file.

**Enemy** — add to `mechanics/enemies.md` under the correct category heading, matching the format of existing entries.

**Rules for writing:**
- Match the format of surrounding entries exactly — no prose, no extra explanation
- Do not add flavour text or lore
- If the item touches a `status: decided` rule, stop and confirm with the user before writing:
  > "This interacts with [X] in [file], which is marked decided. Do you want to proceed?"

After writing, tell the user which file was updated. Do not summarise what was written.
