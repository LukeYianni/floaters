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

## How to Answer Questions

1. Read `glossary.md` to anchor definitions.
2. Read `design-principles.md` to apply the design constraints.
3. Read relevant `decided` files for authoritative rules.
4. Check `rejected-ideas.md` before proposing anything — don't re-propose rejected mechanics.
5. Check `/design-log` for any prior reasoning on the subsystem in question.
6. Flag any open questions your answer touches on.

When generating new rules, present them in the same format as `core-mechanics.md`: named sections, short declarative sentences, bullet lists for triggers and effects.
