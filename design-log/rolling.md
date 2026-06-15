---
status: open
tags: [design-log, rolling, dice, stats]
related: [mechanics/rolling.md, core-mechanics.md]
---

# Rolling System — Design Log

## Pool vs. 2d6+Modifier

Two candidate dice mechanisms were evaluated against the existing result table (1–3 fail / 4–5 partial / 6 full / crit = multiple 6s).

### Pool system (N d6s, take highest)

| Rating | Fail (1–3) | Partial (4–5) | Full (6) | Crit (2+ sixes) |
|--------|-----------|--------------|---------|----------------|
| 0 (2d, take lowest) | 75% | 22% | 3% | 3%* |
| 1 | 50% | 33% | 17% | 0% |
| 2 | 25% | 44% | 28% | 3% |
| 3 | 13% | 45% | 35% | 7% |
| 4 | 6% | 42% | 39% | 13% |

*Rating 0 can only produce a 6 if both dice show 6, so every 6 at rating 0 is automatically a crit.

### 2d6 + modifier (thresholds: ≤6 fail / 7–9 partial / 10+ full)

| Modifier | Fail | Partial | Full |
|----------|------|---------|------|
| −1 | 58% | 33% | 8% |
| 0  | 42% | 42% | 17% |
| +1 | 28% | 44% | 28% |
| +2 | 17% | 42% | 42% |
| +3 | 8%  | 33% | 58% |

### Key differences

**Bell curve vs. pool curve.** 2d6 clusters around the middle — partial success dominates at every modifier. The pool system is flatter; high ratings make full success dominant, not just probable.

**Edge value is uneven in pools.** Adding a die (+1d from Edge) is a large swing at low ratings (rating 1: 50%→25% fail) and a small swing at high ratings (rating 3: 13%→6% fail). In 2d6+mod, +1 is worth the same everywhere. The pool system makes Edge feel like a lifeline at low skill; 2d6+mod makes it a flat, consistent bonus.

**No natural crits in 2d6+mod.** Multiple 6s emerge naturally from pool rolling. 2d6 has no equivalent without a bolt-on rule.

**Higher floor in 2d6+mod.** Rating 0 in the pool system is harsh by design (75% fail). 2d6 at −1 mod gives a 42% shot at partial or better. If an untrained character in danger should feel genuinely at risk, pools make that case harder.

### Decision

Leaning toward **pool system**, capped at rating 0–3 rather than 0–4. Maximum rating 3 still fails 13% of the time, keeping stakes present even for specialists.

---

## Stat Count and Granularity

Current rolling.md uses 9 actions grouped under 3 characteristics (Grit / Deft / Guile).

**Problem identified:** Action labels do too much fictional work. "Hunt" covers both sniping and tracking — very different actions. Multiple actions can plausibly apply to the same situation (flashbang: Break? Guile?), creating table debate at the wrong moment.

**Root cause:** The axis is "what you're doing" rather than "what part of yourself you're using." Stats solve this by shifting the label to the character, not the fiction.

### Options under consideration

**Option A — Collapse to 3–5 broad stats, no actions.**
Rolls against a stat directly. Differentiation comes entirely from perks. Simpler, less debate, but puts heavy weight on the perk system.

**Option B — Daggerheart-style tags.**
Broad stats plus short proficiency phrases (e.g. "sniping," "fast-talk"). If a phrase applies to the roll, add +1d. Specificity without action ratings. Creates a soft layer of nuance without a separate tracked number.

**Option C — Hierarchy (stat → action → specialty).**
Stat (0–2) → Action (e.g. Shoot, 0–3) → Specialty (e.g. Sniper, 0–1). Pool = sum of all applicable dots. Maximum possible character differentiation, but potentially high complexity and bookkeeping.

These options are not yet evaluated against design principles. See open questions below.

---

---

## Stat Shape — What Was Explored

### The problem with 3 stats

The current three characteristics (Grit / Deft / Guile) have a coverage problem:

- **Guile is overloaded.** It currently groups deception, manipulation, persuasion, hacking, investigation, and knowing what's worth salvaging. These are different enough in fiction that lumping them under one word flattens meaningful character distinctions.
- **No command axis.** Guile covers the cunning social approach (manipulation, deception). There is no stat for raw authority — commanding a room, inspiring a crew, making someone back down through force of presence rather than words.
- **No technical axis.** Hacking, drone operation, surgery, and engineering are all "smart" but distinct from social cunning. A setting built around technology probably wants to separate these.

### Proposed expansions

**4 stats: Grit / Deft / Guile / Smarts**
Split Guile into social cunning (Guile) and technical/logical aptitude (Smarts). Hacking, Mech Controller, Biomechanics, and Investigator all move to Smarts. Cleaner than current, but still no command axis.

**5 stats: Grit / Deft / Guile / Smarts / Resolve**
Add Resolve for command, force of will, and authority. Grit stays physical (endurance, brute force). Resolve covers psychological projection outward — making others follow, not breaking under pressure. Enduring's starting ability probably moves to Resolve.

Mapping against specialisms:
| Specialism | Stat |
|---|---|
| Enduring | Resolve |
| Killing | Grit or Deft by approach |
| Explosives | Grit (brute) or Deft (precise placement) |
| Hacking | Smarts |
| Mech Controller | Smarts |
| Biomechanics | Smarts |
| Investigator | Smarts |
| Infiltrator | Deft (physical) or Guile (social) |
| Salvager | Smarts (valuation) or Deft (extraction) |
| Movement | Deft |

**6 stats: adding Willpower**
Raised as a possible split of Resolve into outward-facing command (Resolve) and inward mental strength (Willpower — resisting coercion, not breaking under pressure). Not evaluated. Six stats risks violating the minimal bookkeeping principle.

### Where it was left

The 5-stat shape (Grit / Deft / Guile / Smarts / Resolve) was the furthest developed, with a clean fictional axis for each. The Guile/Resolve boundary — both affect social situations — is the one overlap to watch. The distinction holds: Guile works the angle (cunning, leverage, words), Resolve doesn't move (authority, presence, will).

The Resolve/Willpower question was not resolved. Whether these are one stat or two, and what the right name is, remains open.

Smarts is a placeholder name. Alternatives to consider: Insight, Logic, Neural, Interface.

---

## Open Questions

**Dice mechanism** (leaning resolved)
- Pool system preferred over 2d6+modifier. Rating cap at 0–3 rather than 0–4.

**Stat shape** (unresolved)
- How many stats? 3 / 4 / 5 / 6?
- Is the 5-stat shape (Grit / Deft / Guile / Smarts / Resolve) right, or does Resolve need to split into Resolve + Willpower?
- What is the right name for the technical/logic stat? (Smarts is a placeholder)
- Is the Guile/Resolve social boundary clear enough to hold at the table without GM calls?
- Does character differentiation need to live in the dice pool at all, or is the perk system sufficient to carry it?

**Granularity below stats** (unresolved)
- Option A: stats only, no sub-actions. Differentiation through perks.
- Option B: Daggerheart-style tags — broad stats plus phrases that add +1d if applicable. Adjudication risk.
- Option C: BitD-style hierarchy — stat → action → specialty, pool = sum. High bookkeeping.
- None of these were evaluated against design principles. Not yet a decision.
