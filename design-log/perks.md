---
subsystem: perks
tags: [design-log, perks, specialism, moves]
---

# Perks — Design Log

## Specialism Identity: Hard Gates vs. Named Moves

### What was decided

Specialisms make characters meaningfully distinct through **named moves with specific fictional triggers**, not through exclusive access to common actions.

Hard gates — things only one Specialism can do — are reserved for things requiring extraordinary fictional permission. Drone operation (Mech Controller) is the current example: operating a drone genuinely requires specialist training that a normal person doesn't have. That gate holds.

Everything else — infiltrating a building, hacking a system, patching a wound, investigating a scene — is open to any character. The Infiltrator is not the only one who can sneak. They are the one who has specific named moves that fire off their particular method of sneaking, producing qualitatively different and mechanically richer outcomes than an unspecialised character attempting the same thing.

### Why fictional gating for common actions was rejected

Fictional gating for things like stealth felt wrong because everyone should be able to sneak into a building — some people are just better at it. Saying "only the Infiltrator can attempt infiltration" is both fictionally false and mechanically heavy-handed. It closes off the fiction rather than shaping it.

### What makes a Specialism distinct instead

The Stonetop playbooks are the reference model here. The Fox doesn't own stealth — it has **Catlike** (*when you carry light and move with care, you move silently and remain unseen*) and **Burgle** (*when you sneak on your own into a dangerous place, roll +INT and pick from specific outcomes*). The trigger is fictional, the output is specific. Anyone can sneak; the Fox sneak produces a mechanically distinct result because the Fox has moves that fire off doing it the Fox way.

The pattern: **specific fictional trigger → specific outcome with options**, often crew-feeding.

A good Specialism move is not "+1d to stealth rolls." It is: *when you [do your thing in your particular way], [specific outcome that rewards doing it that way]*. The trigger has texture — it asks something of the fiction, not just "when you attempt X." The outcome has options — it gives the player decisions, not just a number.

### What this means for the perk list

The current perk list has moves at the top (the starting abilities, which are already written in this style) and generic modifiers lower down. The perk list needs to be rewritten so that perks are named moves in the Stonetop style throughout — specific triggers, specific outcomes, ideally crew-feeding at higher tiers.

This is the primary work needed to make Specialisms feel like genuine identities rather than labelled stat bonuses.

### On the Specialism perk discount

A perk discount is a secondary mechanism — it nudges players toward deepening their Specialism by making it cheaper. It is conceptually sound but only earns its place once the perk lists are developed enough that "going deeper" is a clearly rewarding path. Deferred until perk lists are playtested.

The more fundamental fix is making the perks themselves worth wanting, not making them cheaper.

### Reference

See `references/stonetop/playbooks.md` for the full analysis of how Stonetop handles this distinction across all nine playbooks.

---

## Biomechanics Perks — Design Direction

### The minigame framing

Biomechanics (and Mech Control) are intentionally structurally different from other Specialisms. The player builds a personal constellation of augmentations over time — closer to D&D 5e Eldritch Invocations than to a standard perk list. The combination feels personal; the minigame is in the accumulation and the choices made.

### What needs rewriting

The current Robotic Leg and Robotic Arm perks offer pick-one-from-a-list options, but the options are passive fictional facts ("the leg is supernaturally strong") rather than triggered moves. This means they don't fire in play — they're character creation decisions dressed as perks.

### The rewrite direction

Keep the modular pick-from-a-list structure. Keep the body modification framing — these are part of the character, not items. But rewrite every option as a **triggered move or specific fictional permission with mechanical teeth**.

Examples of the pattern:
- "Supernaturally strong leg" → *When you kick something or someone, treat it as a heavy weapon.*
- "Fingers sharp to a blade point" → a named move that fires when attacking unarmed.
- "Shock on touch" → *When you grab hold of someone and discharge, they are stunned and cannot act until they break free.*

Every augmentation option should add something the player can **do**, not just something that is **true** about their character. The fingerprint mimicry option on Robotic Arm is the closest to this already — it creates specific fictional opportunities and is worth keeping as a reference point.

The higher-tier perks (Neural Link, Mental Malware, Neural DDoS) follow naturally from this: they are augmentations that escalate in power and weirdness, pushing further from human. That arc should be legible across the full Biomechanics perk list.

---

## Enduring Perks — Design Gaps

### No Tier 3 capstone
Fuelled by Blood was moved to Tier 2, leaving no Tier 3 perk for Enduring. The capstone should answer: what does the Enduring character look like at their absolute peak? Directions to consider: genuine unkillability, terrifying presence that makes enemies hesitate, or a big crew-feeding moment.

### No crew-feeding perks beyond the starting ability
Tank, Tank 2, Experienced Recovery, and Fuelled by Blood all benefit only the Enduring player. The design principles require individual excellence to feed crew success. At least one perk — likely the Tier 3 capstone — should create crew momentum or opportunity, not just personal durability.
