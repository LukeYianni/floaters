---
status: open
tags: [planning]
---

# To Do

A comprehensive list of what needs to exist for Floaters to be playable as an ongoing campaign. Update this as content is migrated from Notion or written from scratch.

---

## Blocking — the game cannot run without these

- [x] **Wound system** — wound tiers (Critical / Major / Minor), dice penalties per tier, wound slots, recovery
- [x] **Clock and tick system** — what a clock is, how many ticks fill one, types of clocks, what happens when one fills
- [x] **Conditions** — resolved; no named conditions list. GM adjudicates advantage creation via position/effect shift. Documented in `mechanics/rolling.md`.
- [x] **Character creation procedure** — step-by-step process for making a character

---

## Needed for an ongoing campaign

- [ ] **Advancement** — XP costs, how action ratings improve, how perks are acquired, whether characters can buy outside their Specialism
- [ ] **Ship system** — ship stats, rooms, damage, upgrades
- [ ] **Mission and scenario structure** — how a session starts, escalates, and ends in an open format
- [ ] **GM tools** — running antagonists, setting position and effect, managing clocks between sessions, pacing
- [ ] **GM moves list** — a structured set of soft and hard moves the GM makes in response to rolls and fiction. Stonetop's move list is a useful reference. Prevents GM improvisation from being arbitrary.
- [ ] **Threat framing** — a structured format for writing up antagonists: type, impulse, escalating consequences (grim portents), and a terminal outcome (impending doom). Gives antagonists a life beyond individual scenes and makes their pressure feel inevitable. Stonetop's Threats chapter (p.277) is the direct reference.
- [ ] **NPC creation procedure** — a lightweight GM tool for making NPCs quickly: name, concept, instinct, connections, and stats only if needed. Stonetop's NPC chapter (p.453) is the reference. Followers are covered; this is for NPCs who aren't followers.
- [ ] **Finds and intel system** — a structured way to introduce rare tech, artifacts, and valuable information through play. How finds are identified, what unlocking them requires, how they change over time. Stonetop's Arcana and Discoveries systems (p.421–447) are the reference.
- [ ] **Location/site design** — a framework for creating interesting operational locations: what makes a site distinctive, how to represent it mechanically, how to run it at the table. Stonetop's Sites chapter (p.345) is the reference.
- [ ] **Campaign and season structure** — how the game progresses across multiple sessions and seasons. How threats escalate over time, how the crew's situation changes, how to bring a season to a satisfying close. Stonetop's "The Game Ongoing" chapter (p.571) is the reference.
- [ ] **Love letters** — a tool for starting a new season or catching up players who missed sessions. A short piece of fiction addressed to a character, describing what happened to them off-screen and ending with a roll that shapes how they enter the new situation. Stonetop's Writing Moves & Love Letters chapter (p.549) is the reference.
- [ ] **Setting overview** — world context, factions, enough for a GM to improvise from

---

## Follower system extensions

- [ ] **Group followers** — rules for followers with the *group* tag: shared resilience pool, individual members standing out over time, directing the group as a whole vs. directing individuals. Deliberately omitted from the initial draft; add once the base system has been tested. See `design-log/followers.md` for why it was deferred.
- [ ] **Follower advancement** — can followers grow? Can tags change, instincts shift, resilience increase? Stonetop handles this via between-session review. Needs a deliberate decision for Floaters.

---

## Content gaps in existing systems

- [ ] **Modifications system** — weapons list modifications as a distinct column; no rules define how modifications work
- [ ] **Weapon abilities list** — referenced by the Killing Specialism; does not exist
- [ ] **Undefined Specialism starting abilities** — Explosives, Hacking, and Stealth Specialisms have no defined starting ability
- [ ] **Unassigned perks** — 6 perks in `mechanics/perks.md` have no Domain: Data Scrounger, Side Hustle, I Know a Guy Who Knows a Guy, Understand the Model, Expert Tracker, Generative Generator
- [ ] **Playstyle clarification** — confirm whether Specialism and Playstyle are the same thing, or define both and their relationship
- [ ] **Fortune rolls** — referenced by the Good Luck Charm perk; not defined anywhere

---

## Open questions that block adjudication

- [ ] **Flow State duration** — full scene or fixed number of actions? (see `open-questions.md`)
- [ ] **Perk access outside Specialism** — can characters buy perks from other Domains, and if so at what cost?
- [ ] **Domains integration** — do Domains modify rolls directly, or only gate abilities and triggers?
- [ ] **Doctor / Medic playstyle** — Biomechanics partially covers this; needs a deliberate decision

---

## Fix list from audit

Issues identified in `audit-report.md` that need resolving once the above is in place.

- [ ] Cleave, Parry, and Spread each exist as both a free tag and a costed weapon move — decide which version is correct and remove the other
- [ ] Confuse Senses weapon move uses Apocalypse World resolution syntax — rewrite in Floaters terms
- [ ] Scoped tag uses +1/−1 modifier notation — rewrite as +1d/−1d or define what the modifier means
- [ ] Downtime tool wear contradicts equipment rules — one must change
- [ ] Inspirational perk generates Flow through downtime — review against Principle 8
- [ ] Resistance Edge spend not listed in core-mechanics.md — add it or remove it from rolling.md
- [ ] Sneaky tag used on Dagger but not defined in weapon-tags.md
