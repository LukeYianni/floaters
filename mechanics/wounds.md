---
status: draft
tags: [mechanics, wounds, harm, recovery]
related: [mechanics/rolling.md, mechanics/equipment.md, mechanics/downtime.md, core-mechanics.md]
---

# Wounds

## Purpose

Wounds create escalating pressure and meaningful decisions without stalling play. Three tiers of severity carry distinct fictional and mechanical weight. Recovery is a downtime investment, not an automatic reset.

---

## Wound Tiers

| Tier | Penalty | Slots |
|------|---------|-------|
| **Minor** | Limited effect on actions using the affected body part | 2 |
| **Major** | −1d to actions using the affected body part | 2 |
| **Critical** | Assist from teammate or spend 1 Edge to act | 1 |

---

## Taking Wounds

Wounds are consequences assigned by the GM. Position sets the default tier:

- **Controlled** → Minor wound
- **Risky** → Major wound
- **Desperate** → Critical wound

**Resistance** (spend 1 Edge, roll relevant action):

| Roll | Outcome |
|------|---------|
| 1–3 | Full wound — no reduction |
| 4–5 | Wound drops one tier (Critical → Major, Major → Minor, Minor → no wound) |
| 6 | Avoid entirely |
| Crit | Avoid and turn it to your advantage |

> Note: Resistance interacts with `mechanics/rolling.md`, which is status: draft.

---

## Wound Slots

Each character has:
- 2 **Minor** slots
- 2 **Major** slots
- 1 **Critical** slot

**Overflow**: if a wound arrives at a fully occupied tier, it upgrades to the next tier.

**Taken out**: if a wound would overflow beyond Critical, the character is dead.

---

## Wound Penalties

When a wound is taken, the GM and player agree which body part is affected based on fiction. Penalties apply only to actions that rely on that body part. Penalties do not stack.

- **Minor**: limited effect on actions using the affected body part.
- **Major**: −1d to actions using the affected body part.
- **Critical**: to attempt an action, the character must either be Assisted by a teammate or spend 1 Edge.

> Open question: does the Critical penalty apply to all actions, or only to actions using the affected body part?

---

## Armor

When you would take a wound, you may tick one wear on your armor to downgrade the wound by one tier.

> Note: Armor is defined in `mechanics/equipment.md` (status: draft). This entry is a cross-reference only.

---

## Medical Kit

Suppresses the penalty of one wound for the rest of the day. Does not remove the wound.

- Load 1, Stack 3

> Note: The Medical Kit replaces Stims in `mechanics/equipment.md`. Update that file separately.

---

## Recovery

### Healing Clock

Each character has a **healing clock** with 4 segments. Advance it by taking the Healing downtime action (see `mechanics/downtime.md`).

When the clock fills:
- All wounds shift down one tier (Critical → Major, Major → Minor)
- Minor wounds clear
- Reset the clock to 0 and begin again if wounds remain

A character with only Minor wounds clears them in one completion. A Critical wound requires three.
