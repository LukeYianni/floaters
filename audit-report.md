---
generated: 2026-05-19
---

# Audit Report

## Summary

33 problems found across all six categories. The most severe issues are in orphaned references (15 problems) — large parts of the system reference mechanics that have never been written. Internal contradictions (6 problems) include several cases where tags and weapon moves duplicate each other with different costs, and one wrong resolution system imported from another game. Design principle violations (4) and bookkeeping creep (6) are present but mostly confined to the perks list.

---

## A. Internal Contradictions

**1. Cleave exists as both a tag and a weapon move with different effects and costs.**
- `weapon-tags.md`: Cleave — "Add another target next to you." (free, no cost)
- `weapon-moves.md`: Cleave — "Mark 1 wear to carry through excess damage to another target next to you." (costs wear, different effect)
- The Sword in `weapons.md` lists both the Cleave tag and the Cleave weapon move. It is impossible to adjudicate which applies when.

**2. Parry exists as both a tag and a weapon move.**
- `weapon-tags.md`: Parry — "Spend a wear to roll an action to resist damage from a melee attack."
- `weapon-moves.md`: Parry — "Mark wear to +1 to resist damage (or to use fight instead?)" — includes an unresolved question in the rule text.
- The Sword and Rapier both list Parry as a weapon move; Counterweighted (a tag/modification) overlaps further by also adding a die to resist melee attacks.

**3. Spread exists as both a tag and a weapon move with different costs.**
- `weapon-tags.md`: Spread — "Add an extra target next to the original." (free)
- `weapon-moves.md`: Spread — "Spend 1 ammo to split damage across a group of targets next to each other." (costs ammo, different framing)
- The Shotgun lists both the Spread tag and the Spread weapon move in `weapons.md`.

**4. Automatic tag and Burst Fire weapon move overlap on the same weapons.**
- `weapon-tags.md`: Automatic — "Spend X ammo to add X damage and X targets to a shot."
- `weapon-moves.md`: Burst Fire — "Spend X ammo to add X damage split between all targets in an area."
- The Assault Rifle has both the Automatic tag and Burst Fire. The Light Machine Gun has Automatic, Burst Fire, and Spray and Pray. When a player fires an Assault Rifle and wants to hit multiple targets, it is unclear which rule applies.

**5. Resistance spend is not listed in decided Edge spend options.**
- `core-mechanics.md` (decided): Edge can be spent to "+1d to your own roll" or "create a small advantage."
- `mechanics/rolling.md` (draft): Adds a third Edge spend: "Spend 1 Edge and roll a relevant action" to resist consequences.
- The resistance spend is not acknowledged or cross-referenced in core-mechanics.md.

**6. Downtime tool wear contradicts equipment tool rules.**
- `mechanics/downtime.md`: Bringing a tool to a downtime action upgrades effect by marking wear on the tool.
- `mechanics/equipment.md`: "Tools are persistent — no wear tracking."
- These cannot both be true.

**7. Confuse Senses uses a different resolution system.**
- `mechanics/weapon-moves.md`: Confuse Senses uses "On a 10+" and "On a 7–9" notation.
- The Floaters rolling system uses 1–3 / 4–5 / 6 / Crit. The 10+/7–9 system is from Apocalypse World / Powered by the Apocalypse and has no defined mapping to the current roll table.

**8. Scoped tag uses modifier notation inconsistent with the dice pool system.**
- `weapon-tags.md`: Scoped — "−1 to rolls when you haven't spent time lining up the shot... +1 when you do."
- `mechanics/rolling.md`: The system uses dice pools (0–4 dice, take highest). "+1" and "−1" are undefined — it is not clear whether these mean +1d/−1d or something else. The Small Blade tag in the same file correctly uses "+1d/−1d" notation; Scoped does not.

---

## B. Decided vs. Draft Conflicts

**1. Rolling.md introduces an Edge spend not present in decided core mechanics.**
- `core-mechanics.md` (decided): The two listed Edge spend options are "+1d to your own roll" and "create a small advantage."
- `mechanics/rolling.md` (draft): Resistance rules add "Spend 1 Edge and roll a relevant action" as a third use.
- This does not contradict the decided content, but it silently extends it. A player reading only core-mechanics.md would not know resistance costs Edge.

---

## C. Implicit Open Question Resolutions

**1. Domains Integration is partially answered by the current draft state.**
- `open-questions.md` asks: "Should domains modify rolls directly, or only gate abilities and triggers?"
- As written across `mechanics/perks.md` and `glossary.md`, Domains are purely organisational — they categorise perks and gate which abilities a character can access. No draft file introduces Domain-based roll modifiers. The question is effectively answered as "gate abilities and triggers only" by the existing draft content, but `open-questions.md` still lists it as open and deferred.

**2. Doctor / Medic Playstyle is partially addressed by Biomechanics.**
- `open-questions.md` states: "A player wanting to play a doctor has no dedicated perks or progression path."
- `mechanics/perks.md` now has the Biomechanics Specialism with the Stabiliser starting ability: "You can heal team members mid-battle." There is also an Experienced Recovery perk in Endurance. The open question has not been updated to reflect this.

---

## D. Orphaned References

**1. Weapon abilities list** — `mechanics/perks.md`, Killing specialism: "choose 3 options from the weapon abilities list (5 on a crit)." This list does not exist anywhere in the repo.

**2. Wound system** — Referenced in three places with no defining file:
- `mechanics/equipment.md`: Stims "ignore one wound's dice penalty" — dice penalties for wounds are never defined.
- `mechanics/perks.md`: Tank has "extra minor wound slot," Tank 2 has "extra major wound slot" — wound slots are never defined.
- `mechanics/equipment.md`: Armor "downgrades the wound by one tier (Critical → Major → Minor)" — wound tiers are never defined.

**3. Clock and tick system** — `mechanics/downtime.md` is built entirely around clocks and ticks but never defines them. What is a clock? How many ticks fill one? What happens when a clock fills? None of this is written.

**4. Fortune rolls** — `mechanics/perks.md`, Good luck charm: "+1 to fortune rolls." Fortune rolls are not defined anywhere.

**5. Conditions** — Multiple files reference conditions without defining them:
- `mechanics/weapon-moves.md`, Covering Fire: "give everyone in a nearby area the pinned condition."
- `mechanics/perks.md`, Slippery Eel: "You can take a condition to escape bondage."
- `mechanics/perks.md`, Sure-step: "disadvantages like Pinned."
No condition list or condition mechanic exists.

**6. Sneaky tag** — The Dagger in `mechanics/weapons.md` has the Sneaky tag. Sneaky does not appear in `mechanics/weapon-tags.md`.

**7. Weapon modifications system** — `mechanics/weapons.md` lists modifications for many weapons (Silenced, Collapsable, Hidden, etc.) as a distinct column from tags. There is no modifications reference file. Several entries in `mechanics/weapon-tags.md` (Concealable, Counterweighted, Electrified, etc.) appear to double as modifications in `weapons.md`, blurring the distinction between tags and modifications with no rule governing the difference.

**8. Playstyle file** — `core-mechanics.md` and `CLAUDE.md` both reference playstyle triggers as a core mechanic ("each playstyle provides reliable ways to generate Edge"). No playstyle file exists. It is also unclear whether "playstyle" and "specialism" are the same thing or different layers of character identity.

**9. Scrap and Tech** — `mechanics/perks.md`, Salvage perks: Needles in a Haystack finds "scrap," Tech Salvager converts "10 scrap into 1 tech." Scrap and Tech are never defined as item types, resource categories, or tracked quantities.

**10. Ship parts** — `mechanics/perks.md`, Salvager and Fixer Upper-2 perks reference salvaging and modifying ship parts. No ship or vehicle system exists.

**11. Home and background** — `mechanics/perks.md`, Good listener: "Push yourself to use another character's home or background." Neither home nor background is defined as a character attribute.

**12. "Cut 1"** — `mechanics/perks.md`, Targeting body parts: "You can cut 1 to target a limb." The term "cut 1" is undefined.

**13. "Hold 1 forward"** — `mechanics/perks.md`, Shared intel: "hold 1 forward for when someone acts on that intel." This is PbtA terminology not defined in the Floaters system.

**14. "Ticks" as character state** — `mechanics/perks.md`, Cut the crap: "You are immune to the effects of an ally's ticks." This use of "ticks" refers to a character state, not the downtime clock ticks defined in `mechanics/downtime.md`. This undefined term shares a name with an existing mechanic.

**15. Movement range** — `mechanics/perks.md`, Sprinter: "move up to three range distances away." Range is defined for weapons (Next to / Nearby / Far / Very Far) in `mechanics/weapon-tags.md` and `mechanics/weapons.md` but movement range for characters is never defined.

---

## E. Design Principle Violations

**1. Inspirational perk violates Principle 8 (No Downtime Dependency).**
- `mechanics/perks.md`, Leadership: "As a downtime action, roll Grit. On a success, the crew starts the next scene with +2 Flow."
- Principle 8: "Resources are generated during action / No reliance on recovery phases."
- This generates Flow — a core resource — through a downtime action, directly contradicting the principle.

**2. Scoped tag rewards preparation over action, violating Principle 3 (Action Over Planning).**
- `mechanics/weapon-tags.md`: Scoped gives a bonus when you "spend time lining up the shot" and a penalty when you don't.
- Principle 3: "Acting decisively is rewarded / Overplanning is discouraged."
- The tag structurally rewards deliberate preparation (waiting, aiming) over decisive action.

**3. Needles in a Haystack generates resources through downtime, violating Principle 8.**
- `mechanics/perks.md`, Salvage: "As a downtime action, sift through scrap and roll a d6: on a 1 find a piece of tech, 2 find ammo, 3 find fuel."
- A weaker violation than Inspirational — it finds items rather than generating Edge or Flow — but it establishes a pattern of downtime resource generation.

**4. Spray and Pray bypasses the core action rating system.**
- `mechanics/weapon-moves.md`: "Spend as much ammo as you would like, and roll that amount of dice rather than an action."
- The core rolling system (`mechanics/rolling.md`) builds pools from action ratings (0–4). Spray and Pray replaces this with an ammo-driven custom pool with no upper bound. This is not a design principle violation per se, but it is an undefined exception to the established resolution system with no governing rule.

---

## F. Bookkeeping Creep

**1. Ammo tracking.** Ranged weapons track ammo per shot (4–6 shots). This is per-weapon tracking on top of Edge and Flow. Likely intentional but unacknowledged as an exception to the minimal bookkeeping principle.

**2. Wear tracking across multiple items.** Armor, drones, and (implicitly) tools each have their own wear tracks. A Mech Controller with armor and a drone is tracking two separate wear tracks plus Edge and Flow.

**3. Consumable stack tracking.** Equipment consumables track uses within a slot (Stims: 3 uses, Smoke Grenades: 2, etc.). Per-item use tracking for every consumable carried.

**4. Clock tracking.** `mechanics/downtime.md` introduces clocks for healing, repair, advancement, and long-term projects — potentially four separate clocks per character. The clock mechanic itself is undefined (see D.3), but if defined, would represent significant tracking overhead.

**5. Wound slot tracking.** Tank and Tank 2 perks add minor and major wound slots, implying characters track wounds in named slots. The wound system is undefined (see D.2), but named wound slots suggest a per-wound state tracker.

**6. Scrap as a counted resource.** `mechanics/perks.md`, Salvage: Tech Salvager converts "10 scrap into 1 tech." Scrap is a counted numeric resource — a direct violation of the minimal bookkeeping principle if formalised.
