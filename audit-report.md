---
generated: 2026-06-26
---

# Audit Report

## Summary

54 problems found across all six categories. The most severe cluster is in category A (Internal Contradictions): the enemy/follower subsystems use entirely different damage models from player-facing wound mechanics, and three weapon tags are duplicated by weapon moves with different and incompatible effects. Category D (Orphaned References) is the densest: 22 items reference mechanics, lists, or systems that don't exist. Bookkeeping creep (F) is significant — the system as currently written tracks at least 15 separate resources beyond Edge and Flow.

---

## A. Internal Contradictions

**1. Enemy armor vs. player armor — two incompatible models**
- `mechanics/enemies.md`: "Armor reduces incoming damage by its rating. Subtract armor from the damage dealt before applying it to resilience." Armor 1 vs. a pistol (damage 1) = zero damage through.
- `mechanics/equipment.md` and `mechanics/wounds.md`: Player armor has wear (1–2 uses). Tick one wear to downgrade a wound by one tier. No damage number is subtracted.
- Enemy armor is a flat numeric damage reducer applied to a resilience pool. Player armor is a wound-tier downgrader with uses. These are two different systems occupying the same fictional space. A player fighting an armored enemy and that enemy attacking a player use different underlying models with no bridge between them.

**2. Enemy resilience vs. player wounds — two incompatible models**
- `mechanics/enemies.md`: Enemies have a numeric Resilience stat. Weapon damage (a number) is subtracted from it each hit. "Damage from weapons is a number; subtract it from resilience each hit."
- `mechanics/wounds.md`: Players have tiered wound slots (2 Minor / 2 Major / 1 Critical). Damage doesn't subtract from a number — it fills a slot at a GM-assigned tier.
- `mechanics/followers.md`: Followers use a separate circle-track with 2–4 boxes, filled one per hit regardless of weapon damage.
- Three different damage absorption systems are in play simultaneously with no cross-system rules.

**3. Cleave: tag vs. weapon move — different effects**
- `mechanics/weapon-tags.md`: "Cleave — Add another target next to you." (Free, passive.)
- `mechanics/weapon-moves.md`: "Cleave — Mark 1 wear to carry through excess damage to another target next to you." (Costs wear, requires excess damage.)
- `mechanics/weapons.md`: Sword has both the Cleave tag AND the Cleave weapon move listed simultaneously. A player cannot determine which rule applies when they use the Sword.

**4. Spread: tag vs. weapon move — different costs and effects**
- `mechanics/weapon-tags.md`: "Spread — Add an extra target next to the original." (Free, passive.)
- `mechanics/weapon-moves.md`: "Spread (Shotgun) — Spend 1 ammo to split damage across a group of targets next to each other." (Costs ammo, damage splits rather than adds.)
- `mechanics/weapons.md`: Shotgun has both the Spread tag AND the Spread weapon move. The tag adds a target for free; the move costs ammo and changes how damage works. Both apply to the same weapon simultaneously.

**5. Parry: tag vs. weapon move — incomplete and contradictory**
- `mechanics/weapon-tags.md`: "Parry — Spend a wear to roll an action to resist damage from a melee attack."
- `mechanics/weapon-moves.md`: "Parry — Mark wear to +1 to resist damage (or to use fight instead?)." The move is unfinished with a parenthetical question unresolved.
- `mechanics/weapons.md`: Sword and Rapier both list Parry as a weapon move. The tag and the move have different (and one incomplete) descriptions.

**6. Scoped tag uses numeric modifier language inconsistent with the dice pool system**
- `mechanics/weapon-tags.md`: "Scoped — −1 to rolls when you haven't spent time lining up the shot, or against fast-moving opponents. +1 when you do."
- `mechanics/rolling.md`: The system uses dice pools — add or remove dice, not numeric modifiers. "+1 to rolls" has no defined meaning in the resolution system. The established language is "+1d" or "roll with disadvantage (two dice, take lowest)."

**7. Action rating cap contradicts action rating range**
- `mechanics/rolling.md`: "The pool is built from their rating in the relevant action (0–4 dice)." Ratings explicitly go 0–4.
- `mechanics/advancement.md`: "Action ratings cap at 2. An action rating already at 2 cannot be upgraded further."
- `mechanics/character-creation.md`: "No action may exceed 2 at the end of creation."
- Characters can never have an action rating above 2. The 0–4 range in rolling.md describes a pool size that is permanently unreachable. A rating of 3 or 4 dice is described but cannot be obtained.

**8. Automatic tag vs. Burst Fire weapon move — different spending structures**
- `mechanics/weapon-tags.md`: "Automatic — Spend X ammo to add X damage and X targets to a shot (there must be X targets)." Adds damage and targets.
- `mechanics/weapon-moves.md`: "Burst Fire (Assault Rifle, LMG) — Spend X ammo to add X damage split between all targets in an area." Damage splits across targets rather than adding per target.
- Assault Rifle and LMG both have the Automatic tag and the Burst Fire weapon move. A player using an Assault Rifle can trigger both; the effects are contradictory.

**9. Core Loop XP source is contradicted by advancement rules**
- `core-mechanics.md` (decided): Core Loop step 4 is "Gain XP through crew behaviour."
- `mechanics/advancement.md` (draft): XP comes from two sources — failure (1–3 roll results) and end-of-session questions. Crew XP is explicitly flagged as "Optional" and "not yet decided."
- The decided file enshrines crew-behaviour XP as a core loop element; the draft advancement file says it doesn't exist yet.

**10. Medical Kit note in wounds.md references a stale state in equipment.md**
- `mechanics/wounds.md`: "Note: The Medical Kit replaces Stims in mechanics/equipment.md. Update that file separately."
- `mechanics/equipment.md`: Already shows a Medical Kit, not Stims. The replacement has been made but the note was not removed. The note implies equipment.md still has Stims when it doesn't.

---

## B. Decided vs. Draft Conflicts

**1. Edge spend "create a small advantage" has no mechanical backing**
- `core-mechanics.md` (decided): "Spend Edge (personal benefit) — Create a small advantage."
- `mechanics/rolling.md` (draft): Lists two uses of Edge: "Push Yourself — spend 1 Edge to add 1d" and the Resistance move "Spend 1 Edge and roll a relevant action." There is no mechanic called "create a small advantage." No roll, no outcome table, no fictional framing.
- **Severity**: The decided file promises a spend option that the draft rules system doesn't support. A player reading both files cannot adjudicate what "create a small advantage" means.

**2. Flow abilities are mentioned but never defined**
- `core-mechanics.md` (decided): "Spend Flow to — Activate Flow abilities / Trigger Flow State." Flow State also "Unlocks Flow abilities."
- No file anywhere defines what Flow abilities are, how they are purchased, or how they are spent. The decided file names them as a spend option; no draft file defines them.
- **Severity**: A core resource spend listed in a decided file has no corresponding mechanic anywhere.

**3. Design Principle 8 (No Downtime Dependency) vs. Training downtime action**
- `design-principles.md` (decided), Principle 8: "No Downtime Dependency — Resources are generated during action / No reliance on recovery phases."
- `mechanics/downtime.md` (draft): "Training — Advance a skill or attribute. Roll and apply ticks to an advancement clock."
- A downtime activity explicitly for advancing skills exists in a draft file, directly contradicting the decided principle against downtime dependency. `mechanics/advancement.md` partially addresses this by saying there is no downtime gate on XP spending — but the Training activity still exists as a written rule with no note that it conflicts.
- **Severity**: Draft silently maintains content that the decided principle prohibits.

---

## C. Implicit Open Question Resolutions

**1. Individual XP drives — partially answered, still listed as open**
- `open-questions.md` asks: "What format do personal XP drives take? How many drives does a character have? What counts as a valid drive?"
- `mechanics/advancement.md` answers this: two personal end-of-session questions (Instinct demonstration; meaningful relationship shift), explicitly tied to the Instinct authored at character creation. The format is question-based, not free-form. The number is two.
- `open-questions.md` still lists all four sub-questions as open.

**2. Domains integration — answered by implementation, still listed as open**
- `open-questions.md` asks: "Should domains modify rolls directly, or only gate abilities and triggers? (Currently deferred.)"
- `mechanics/perks.md` implements Domains purely as perk trees. No Domain modifies a roll directly anywhere in the file. The system as written has resolved this in favor of "gate abilities only."
- `open-questions.md` still lists this as an open, deferred question.

---

## D. Orphaned References

**1. Weapon abilities list — referenced but doesn't exist**
- `mechanics/perks.md`: Killing Specialism — "choose 3 options from the weapon abilities list." Ballistics perk "Killer" — "choose one extra option from the list of options you have."
- No weapon abilities list exists anywhere in the repository.

**2. Specialism name mismatch: "Infiltrator" vs. "Covert"**
- `mechanics/perks.md` Specialism table: Lists "Infiltrator" as a Specialism.
- `mechanics/perks.md` perk domain section: The domain is titled "Covert" with perks like "Ambusher." No "Infiltrator" perk section exists.
- A player choosing the Infiltrator Specialism has no associated perk tree.

**3. Ship creation system — referenced but doesn't exist**
- `mechanics/character-creation.md`: "Ship Creation — As a group, build the crew's ship together. (Ship creation procedure: see ship system, not yet written.)"
- No ship system file exists.

**4. Stun — referenced but not defined**
- `mechanics/perks.md`: Robotic Arm "Shock discharge: they cannot act until they physically break free or the scene changes. (Open: stun needs a formal mechanical definition.)"
- No stun condition is defined anywhere.

**5. Extra wound slots — referenced but wound system has fixed slots**
- `mechanics/perks.md`: Endurance perk "Tank — You have an extra minor wound slot." "Tank 2 — You have an extra major wound slot."
- `mechanics/wounds.md`: Wound slots are fixed at 2 Minor / 2 Major / 1 Critical. There is no mechanic for adding slots.

**6. Fortune rolls — referenced but not defined**
- `mechanics/perks.md`: Leadership perk "Good luck charm — +1 to fortune rolls."
- No fortune roll mechanic exists anywhere in the repository.

**7. "Ticks" as ally behavior — undefined term collision**
- `mechanics/perks.md`: Leadership perk "Cut the crap — You are immune to the effects of an ally's ticks."
- "Ticks" elsewhere in the system means filling clock segments. No "tick" as a personal condition or behavioral state is defined.

**8. "Cut 1" — referenced but not defined**
- `mechanics/perks.md`: Ballistics perk "Targeting body parts — You can cut 1 to target a limb."
- "Cut 1" is not defined anywhere.

**9. "+1 effect to results when healing" — no mechanism defined**
- `mechanics/perks.md`: Endurance perk "Experienced Recovery — You get +1 effect to results when healing."
- Effect level is set by the GM based on fictional positioning. No mechanic exists for a perk to shift effect level.

**10. "Aimed down a sight" — no mechanic defined**
- `mechanics/perks.md`: Ballistics perk "Boom Headshot — When you successfully kill a target that you have aimed down a sight to hit, you still gain the scoped benefits until you either miss or are attacked."
- No "aim down sights" mechanic exists. The Scoped tag does not describe an aiming state that persists across turns.

**11. Needles in a Haystack — result for 4-6 unspecified**
- `mechanics/perks.md`: Salvage perk "Needles in a Haystack — roll a d6: on a 1 find a piece of tech, 2 find ammo, 3 find fuel."
- Results for 4, 5, and 6 are not specified.

**12. Tags defined but applied to no weapon: Pull, Knock Back, Small Blade**
- `mechanics/weapon-tags.md`: Defines Pull, Knock Back, and Small Blade.
- `mechanics/weapons.md`: None of these tags appear on any weapon in the weapon table.

**13. Concealable and Magnetic listed as modifications in weapons.md but as tags in weapon-tags.md**
- `mechanics/weapons.md`: Dagger and Pistol modifications include "Concealable." Dagger modifications include "Magnetic."
- `mechanics/weapon-tags.md`: Both "Concealable" and "Magnetic" are defined as tags, not modifications. No rule explains how a modification differs from a tag mechanically.

**14. Multi-drone control referenced in perks but not defined in drones.md**
- `mechanics/perks.md`: Mech Control perk "Split Focus — control two fully independent mechs simultaneously." "Hive Mind — control a swarm."
- `mechanics/drones.md`: Describes only a single drone. No rules for controlling two independent drones or a swarm are written.

**15. "Weighted Strike: +1 roll" — undefined modifier**
- `mechanics/perks.md`: Melee Combat perk "Weighted Strike — mark 1 wear for +1 roll to an attack."
- "+1 roll" is not defined. The system uses +1d.

**16. Threat format for escalated followers — undefined**
- `mechanics/followers.md`: "the former follower may become a threat."
- No threat format is defined in any mechanics file.

**17. Movement Specialism starting ability — absent**
- `mechanics/perks.md`: Movement Specialism — "parked — fantasy not yet defined." Starting items are listed but the starting ability is blank.
- The Movement perk domain has a written perk tree, but the Specialism that anchors it has no starting ability.

**18. "Relevant skill" in equipment — undefined term**
- `mechanics/equipment.md`: "Without the relevant skill, they roll zero dice."
- The system uses action ratings, not skills. "Relevant skill" has no defined meaning.

**19. Neural Link coordination — undefined mechanic**
- `mechanics/perks.md`: Biomechanics perk "Neural Link — When you coordinate via neural link before an ally acts, they roll with +1d."
- No "coordinate via neural link" mechanic is defined. It's unclear how this differs from a normal Assist or whether it stacks with one.

**20. Stims — referenced in wounds.md as the old item being replaced, but already gone**
- `mechanics/wounds.md`: "Note: The Medical Kit replaces Stims in mechanics/equipment.md."
- "Stims" appear nowhere in `mechanics/equipment.md`. If perks or other rules referenced Stims before removal, those references are not identified.

**21. Sensor Kit — associated perk domain doesn't exist**
- `mechanics/equipment.md`: Sensor Kit domain listed as "Tracking / Sensing."
- No "Tracking" or "Sensing" perk domain exists in `mechanics/perks.md`.

**22. "Good listener" — mechanism undefined**
- `mechanics/perks.md`: Leadership perk "Good listener — Push yourself to use another character's home or background."
- Home and background grant +1 action rating to specific actions at creation only. No mechanic exists for "using" someone else's home or background after creation.

---

## E. Design Principle Violations

**1. Inspirational perk generates Flow through safe downtime**
- `mechanics/perks.md`: "Inspirational — As a downtime action, roll Grit. On a success, the crew starts the next scene with +2 Flow."
- `design-principles.md`, Principle 4: "Risk is the Engine — Taking risks generates resources / Safe play does not."
- `design-principles.md`, Principle 8: "No Downtime Dependency — Resources are generated during action / No reliance on recovery phases."
- Flow is generated in downtime without any risk-taking.

**2. Training downtime action contradicts No Downtime Dependency**
- `mechanics/downtime.md`: "Training — Advance a skill or attribute. Roll and apply ticks to an advancement clock."
- `design-principles.md`, Principle 8: "No Downtime Dependency — Resources are generated during action / No reliance on recovery phases."
- The Training activity establishes downtime as a vector for advancement, which the principle explicitly prohibits.

**3. Needles in a Haystack generates resources without risk**
- `mechanics/perks.md`: "Needles in a Haystack — As a downtime action, sift through scrap and roll a d6: on a 1 find tech, 2 find ammo, 3 find fuel."
- `design-principles.md`, Principle 4: "Risk is the Engine — Taking risks generates resources / Safe play does not."
- A downtime roll for random resource generation with no fictional risk and no stated consequence for 4–6.

**4. Generative Generator produces information without rolls or fictional positioning**
- `mechanics/perks.md`: "Generative Generator — it can answer questions in its domain without a roll, and works autonomously on its purpose during downtime."
- `design-principles.md`, Principle 10: "Fiction-First Mechanics — Resource generation requires fictional justification / Mechanics follow narrative positioning."
- An asset that produces information without a roll removes the fiction-first trigger entirely.

---

## F. Bookkeeping Creep

The following tracked resources and states exist in the system beyond Edge (0–2) and Flow (0–6):

**Per character:**
1. **XP pool** (`mechanics/advancement.md`) — accumulates indefinitely, no cap defined.
2. **Wound slots** (`mechanics/wounds.md`) — 2 Minor / 2 Major / 1 Critical slots; each slot records its content.
3. **Healing clock** (`mechanics/wounds.md`, `mechanics/downtime.md`) — 4-segment clock per character, tracked separately from wounds.
4. **Action ratings** (`mechanics/rolling.md`) — 9 separate ratings (0–2 each) per character.

**Per item/gear:**
5. **Armor wear** (`mechanics/equipment.md`) — 1–2 uses per armor piece.
6. **Consumable stacks** (`mechanics/equipment.md`) — per-consumable use counts (stack 1–3 per item type).
7. **Ammo counts** (`mechanics/weapons.md`) — per-weapon ammo tracked for every ranged weapon carried (2–6 per weapon).
8. **Tool/item wear** (referenced throughout perks) — wear on various items marked during play.

**Per drone:**
9. **Drone wear** (`mechanics/drones.md`) — 3-segment wear track per drone.

**Per follower:**
10. **Follower Loyalty** (`mechanics/followers.md`) — 0–3 per follower.
11. **Follower resilience** (`mechanics/followers.md`) — 2–4 circles per follower.

**Per enemy:**
12. **Enemy resilience** (`mechanics/enemies.md`) — numeric value subtracted on each hit; separate system from player wounds with no shared resolution mechanic.

**Crew/situation:**
13. **Clocks** (`mechanics/clocks.md`) — variable size, unlimited number. Healing, advancement, projects, threats, and situations all use separate clocks simultaneously.
14. **Load tracking** (`mechanics/equipment.md`) — total load tracked against capacity tier (2/4/6).
15. **Holds** (`mechanics/rolling.md`, Defend move) — temporary tokens (up to 3) created by Defend, spent and lost within a scene.
