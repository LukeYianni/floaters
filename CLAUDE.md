# Floaters — LLM Knowledge Base Guide

## What This Is

This repository is the design knowledge base for **Floaters**, a tabletop RPG system. Files here are the authoritative record of design decisions: what the system does, why it does it, what was tried and rejected, and what is still open.

Your job when working with this repo is to help design, refine, and extend the system — answering questions, generating new rules, identifying contradictions, and stress-testing ideas against the design principles.

---

## How to Navigate This Repo

| File | Purpose |
|---|---|
| `CLAUDE.md` | This file. Start here. |
| `glossary.md` | Authoritative definitions for all system terms. Read this before answering any question about a term. |
| `design-principles.md` | The non-negotiable goals of the system. Every mechanic must serve these. Check here when evaluating any new idea. |
| `core-mechanics.md` | The current decided rules: Edge, Flow, Flow State, Crew Types, core loop. |
| `open-questions.md` | Unresolved design decisions. Treat these as prompts for exploration, not settled rules. |
| `rejected-ideas.md` | Ideas that were tried and discarded, with reasons. Never re-propose these without acknowledging why they were rejected. |
| `mechanics/rolling.md` | Core roll mechanic: action pools, result table, position (implicit GM call), effect. Status: draft. |
| `mechanics/perks.md` | The Perks system: Domains, Specialisms, and the full perk list by Domain and Tier. Status: draft. |
| `mechanics/weapons.md` | All weapons with stats (Damage, Ammo, Load, Range, Tags, Modifications, Weapon Moves). Status: draft. |
| `mechanics/weapon-moves.md` | Special actions tied to specific weapons. Status: draft. |
| `mechanics/weapon-tags.md` | Passive weapon properties and their mechanical effects. Status: draft. |
| `mechanics/downtime.md` | Downtime actions, effect scale, antagonist pacing, and downtime activities. Status: draft. |
| `mechanics/followers.md` | Follower system: card format, tags, resilience track, instinct, cost, Loyalty, follower moves, Edge interaction. Status: draft. |
| `mechanics/equipment.md` | Equipment system: carrying capacity tiers, consumable stacking rules, armor. Status: draft. |
| `mechanics/drones.md` | Drone subsystem: deployment, acting through drones, wear, item card format. Status: draft. |
| `mechanics/character-creation.md` | Character creation: the three axes (What Was Home, Why Did You Leave, What Is Your New Home), action rating sources, Specialism selection. Status: draft. |
| `mechanics/clocks.md` | Clocks and progress tracking. Status: draft. |
| `mechanics/wounds.md` | Wound system. Status: draft. |

| `setting/history.md` | The Fall / The Wipe: how Earth was destroyed and how the solar system adapted. |
| `setting/politics.md` | Inter-faction tensions: Mars vs Venus, Floaters, the Moon as neutral ground, the Black Echo. |
| `setting/planets/mars.md` | Mars: authoritarian state, subterranean cities, breakaway communities, the state apparatus. |
| `setting/planets/venus.md` | Venus: floating city-states, the Skyfaring League, Gasrunners, culture and governance. |
| `setting/planets/moon.md` | The Moon: contract economy, fulfillment indices, clan structure, data sanctuaries. |
| `setting/planets/floaters.md` | Floaters as a people: spinners, zero-G communities, nomadic groups, reputation. |
| `setting/factions/ash-network.md` | The Ash Network: Martian rebel confederation, internal factions, tactics, legendary figures. |
| `setting/factions/sapphire-reign.md` | The Sapphire Reign: Venusian floating opera-city, the Conductors' Triumvirate, culture. |
| `setting/factions/black-echo.md` | The Black Echo: solar-system-wide anti-AI paramilitary, Oblivion Gate, Echoes. |
| `setting/factions/breakers-of-the-word.md` | The Breakers of the Word: lunar anti-contract revolutionaries, the Void, underground networks. |

| `campaign/gm-reference.md` | Campaign file conventions and directory structure. Read before adding any campaign content. |
| `campaign/arcs/` | One file per campaign arc: situation, background, pivots, timeline, GM moves. |
| `campaign/threats/` | One file per active threat: instinct, grim portents, clock. Read here to understand what's applying pressure. |
| `campaign/sites/` | One file per location: layout, encounters, GM moves, discoveries. |
| `campaign/npcs/` | NPC profiles and stat blocks grouped by location. |
| `campaign/factions/` | Background on organisations: how they work, not their threat clock. |

As the system grows, files will be organized into subdirectories:
- `/mechanics` — individual subsystem files
- `/characters` — playstyles, abilities, advancement
- `/setting` — world and fiction context

---

## Core Vocabulary

Always use these terms precisely and consistently:

- **Edge** — a personal short-term resource (0–2 per character). Represents individual momentum and opportunity.
- **Flow** — a shared crew resource (0–6). Represents team synergy.
- **Flow State** — a triggered mode when Flow reaches 6. Powerful, short-duration crew boost.
- **Crew** — the player group. Defines group Edge triggers and XP triggers.
- **Playstyle** — individual character role. Defines personal Edge triggers.
- **Domain** — a character's area of expertise (not yet fully defined; see open-questions.md).
- **Assist** — helping another character on their roll (mechanics TBD).

---

## Design Constraints

When generating new rules or evaluating ideas, always check against `design-principles.md`. The core constraints are:

- **Risk is the engine** — resources come from taking risks, not from planning or waiting.
- **Action over planning** — mechanics reward acting, not preparing.
- **Team-first** — individual success should feed crew success.
- **Minimal bookkeeping** — no complex tracking. Small caps on all resources.
- **Fiction-first** — every mechanical trigger requires a fictional justification.

If a proposed mechanic violates any of these, flag it explicitly before suggesting it.

---

## Status Convention

Each file has a frontmatter `status` field:

- `decided` — the mechanic or principle is agreed upon. Treat as authoritative.
- `draft` — the direction is set but details may shift.
- `open` — actively unresolved. Explore freely.

Do not treat `open` content as decided. Do not re-open `decided` content without flagging the contradiction explicitly.

---

## Design Log

The `/design-log` directory contains one file per subsystem, recording what was considered, what was decided, and why. These files capture the reasoning behind decisions — not just the rules themselves.

**Before working on any subsystem, check whether a design log file exists for it.** If it does, read it before proposing changes or additions. This prevents re-opening settled questions and re-treading ground that has already been covered.

| File | Subsystem |
|---|---|
| `design-log/followers.md` | Follower system: tag structure, resilience track, Edge interaction, Loyalty |

---

## Reference Materials

Summaries of relevant rules from other game systems live in `/references/`. Read these before reading any source PDF — they exist to save tokens.

| File | What to use it for |
|---|---|
| `references/stonetop/monsters-and-dangers.md` | Monster format, tags, HP, armor, damage, instinct, moves |
| `references/stonetop/adventure-and-story-arcs.md` | How Stonetop structures campaigns, threats, grim portents, expeditions, and session zero |
| `references/stonetop/npcs-and-followers.md` | NPC creation, portrayal, follower stats, Loyalty, group followers, Persuade mechanics |
| `references/stonetop/encounters-and-sites.md` | Site creation, encounter design, discoveries, hazards, GM moves, the core loop |

If a relevant section hasn't been summarised yet and you need to read the source, the Stonetop PDFs are at `/Users/lukeyianni/Documents/Stonetop/`. Read only the pages needed and add a summary to `/references/stonetop/` afterwards so it doesn't need to be re-read.

Always check `/references/` before reading a source PDF.

---

## How to Answer Questions

1. Read `glossary.md` to anchor definitions.
2. Read `design-principles.md` to apply the design constraints.
3. Read relevant `decided` files for authoritative rules.
4. Check `rejected-ideas.md` before proposing anything — don't re-propose rejected mechanics.
5. Check `/design-log` for any prior reasoning on the subsystem in question.
6. Check `/Users/lukeyianni/Documents/Stonetop/` if the task references Stonetop.
7. Flag any open questions your answer touches on.

**Topic-to-file shortcuts** — read the relevant file immediately when these topics come up, without waiting to be asked:

| Topic | Read first |
|---|---|
| Character creation, session zero, backstory, action ratings, Specialisms | `mechanics/character-creation.md` |
| Arc structure, campaign design, story hooks, faction pressure, adventure design | `references/stonetop/adventure-and-story-arcs.md` |
| Encounter design, site design, locations, hazards, discoveries | `references/stonetop/encounters-and-sites.md` |
| NPC design, NPC portrayal, follower creation, Loyalty | `references/stonetop/npcs-and-followers.md` |
| Clocks, progress tracking, countdowns | `mechanics/clocks.md` |
| Wounds, injury, harm, debilities | `mechanics/wounds.md` |
| Rolling, actions, position, effect | `mechanics/rolling.md` |
| Perks, Domains, abilities, advancement | `mechanics/perks.md` |
| Followers, NPCs, loyalty | `mechanics/followers.md` |
| Downtime, between-session activities | `mechanics/downtime.md` |
| Weapons, gear, equipment, load | `mechanics/weapons.md`, `mechanics/equipment.md` |
| Mars, Martian state, Red Order, Ash Network, rebels | `setting/planets/mars.md`, `setting/factions/ash-network.md` |
| Venus, floating cities, Sapphire Reign, Gasrunners | `setting/planets/venus.md`, `setting/factions/sapphire-reign.md` |
| Moon, lunar economy, contracts, Breakers | `setting/planets/moon.md`, `setting/factions/breakers-of-the-word.md` |
| Floaters, spinners, zero-G communities | `setting/planets/floaters.md` |
| Black Echo, AI, the Wipe, the Fall | `setting/factions/black-echo.md`, `setting/history.md` |
| Factions, politics, inter-planetary tensions | `setting/politics.md` |

When generating new rules, present them in the same format as `core-mechanics.md`: named sections, short declarative sentences, bullet lists for triggers and effects.
