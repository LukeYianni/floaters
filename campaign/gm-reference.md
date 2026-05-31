---
status: draft
tags: [campaign, gm-tools]
---

# GM Reference

Conventions used across all campaign files. Read this before adding a new location, NPC, or scenario.

---

## Directory Structure

```
campaign/
  arcs/        — one file per campaign arc (the story, situation, timeline, pivots)
  threats/     — one file per active threat (instinct, grim portents, clock)
  sites/       — one file per location (layout, encounters, GM moves, discoveries)
  npcs/        — NPC profiles and stat blocks, grouped by location
  factions/    — background on organisations (how they work, not their threat clock)
  gm-reference.md
```

**When you need:** what's applying pressure → read `threats/`
**When you need:** where the crew is → read `sites/`
**When you need:** who someone is → read `npcs/`
**When you need:** how an organisation works → read `factions/`
**When you need:** the arc overview and scenario flow → read `arcs/`

---

## What campaign files are for

Campaign files are GM-facing tools, not player-facing content. They exist to answer the questions you'd otherwise have to improvise cold at the table — what does this place do when players poke at it, what does this NPC want, what happens if the crew ignores this problem.

They don't tell you what to say. They give you pre-thought material to draw from so your improvisation is grounded in the fiction you've already built.

---

## Arc files (`arcs/`)

Each arc file covers a campaign scenario — a situation with stakes, pressure, and a direction it's heading if nobody acts.

Sections:
- **The Situation** — plain statement of what's true right now. No backstory, just current state.
- **Background** — the history that produced the situation, as briefly as it needs to be.
- **Active Threats** — list of threats with links to their threat files.
- **Tonight's Timeline** — what's happening right now, before the crew acts.
- **Key Encounters** — important scripted moments with scenario guidance.
- **The Pivot** — the key revelation or structural turn of the arc.
- **Resolution** — how the arc closes and what carries forward.
- **What Players Can Discover** — the information layer: what's findable and how.
- **GM Moves** — directive prompts written as "when X, then Y."

---

## Threat files (`threats/`)

Each threat is an active pressure on the crew — a thing that moves if left alone.

Sections:
- **Type** — Faction, Villain, Hazard, Countdown, or Web
- **Impulse** — what it does if left alone, in one sentence
- **Stakes** — what the crew specifically stands to lose (personal, not abstract)
- **Grim Portents** — 3–5 escalating steps, each a concrete thing that happens in the fiction
- **Impending Doom** — the final portent; the natural consequence if the clock fills
- **Threat Clock** — how many ticks, and what fills it

### Threat types

**Faction** — an organisation or group applying pressure. Has agency, responds to player action, can be negotiated with or destroyed.

**Villain** — an individual with intent. More personal than a faction. Often has a grim portent clock tied to their awareness of the crew.

**Hazard** — an environmental or systemic danger. Doesn't have intent but advances on its own logic.

**Countdown** — something that will happen regardless. A deadline. The question is whether the crew is in the right position when it does.

**Web** — an entanglement that gets worse as the crew acts. Every move tightens it. Useful for political situations where there's no clean solution.

---

## Site files (`sites/`)

Each site file covers a specific place the crew might spend time in.

Sections:
- **Overview** — 2–3 sentences: what is this place, what does it feel like, what's the core tension living inside it.
- **Factions** (if a large location) — groups with power or presence. Each has: *Want* and *Move*.
- **Key Areas** — specific areas within the location. Each has:
  - Atmosphere — sensory, brief. Enough to put you in the room.
  - What's happening here — current state, not general description.
  - *What happens here* — how this space responds when players engage. Pre-think this so you don't have to invent it cold.
  - GM moves — specific, directive.
- **What Players Can Discover** — the information layer for this location.
- **Open Questions** — things to decide before running this location.

---

## NPC files (`npcs/`)

NPC files are grouped by location. Each significant NPC gets:

**Concept** — one line. Who they are at their core.

**Want** — what they're trying to achieve or protect. This drives every scene they're in.

**Instinct** — what they do by default, unprompted. How they behave when nobody's pushing them.

**Tell** — how they behave under pressure. The specific, playable thing that changes when the situation gets hard.

**Background** — brief relevant history. Only what's needed at the table.

**Stat block** (if they might fight or be fought) — resilience, armor, equipment, instinct, moves. See format in existing NPC files.

---

## Clocks

Each clock has:
- A name
- What fills it (specific triggers, not vague conditions)
- What happens when it fills (the consequence — concrete)

Clocks are not hidden from players unless there's a specific reason. Players knowing a clock exists creates urgency.

Tick clocks when:
- Players take a 6- on a relevant roll
- Time passes without action on the relevant problem
- The fiction demands it regardless of player action

---

## Faction files (`factions/`)

Faction files contain background on how an organisation works — its structure, ideology, methods, and reach. They are not threat files. The threat clock lives in `threats/`. The faction file answers "how does this organisation operate?" not "what is it doing to the crew right now?"
