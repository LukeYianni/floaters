---
status: draft
---

# Weapons

Each weapon has the following stats:

- **Damage** — how much harm it deals on a hit
- **Load** — encumbrance cost to carry
- **Range** — Next to / Nearby / Far / Very Far
- **Tags** — passive properties the weapon has by default (see `weapon-tags.md`)
- **Modifications** — additional tags from `weapon-tags.md` that can be added to the weapon
- **Weapon Moves** — special actions available only with this weapon (see `weapon-moves.md`)

---

## Melee Weapons

| Weapon | Damage | Load | Range | Tags | Modifications | Weapon Moves |
|---|---|---|---|---|---|---|
| Baton | 1 | 2 | Next to | Non-lethal | — | — |
| Dagger | 1 | 1 | Next to | Sneaky, Throwable, Small Blade | Concealable, Counterweighted, Electrified, Magnetic, Multi-tool, Tethered, Throw-balanced | Exploit Vulnerability |
| Hammer | 2 | 2 | Next to | — | — | Wreck |
| Rapier | 2 | 2 | Next to | Parry | Hidden | Disarming Strike |
| Spear | 2 | 2 | Next to | Throwable | Collapsable, Electrified, Throw-balanced | — |
| Sword | 2 | 2 | Next to | Cleave, Parry | Counterweighted, Throw-balanced | — |

---

## Ammo

Ranged weapons use an abstract ammo track with three statuses (left to right):

**Plenty left → Low ammo → All out**

When a move tells you to mark ammo, or the GM calls for it, tick the next status. When you mark **All out**, you cannot use that weapon until you replenish.

---

## Ranged Weapons

| Weapon | Damage | Load | Range | Tags | Modifications | Weapon Moves |
|---|---|---|---|---|---|---|
| Pistol | 1 | 1 | Nearby | — | Concealable, Silenced | Double Tap, Quickdraw, Disarming Shot |
| Shotgun | 2 | 2 | Nearby | Spread, Forceful | — | Wreck |
| Sub-machine Gun | 2 | 2 | Nearby | Automatic | Collapsable, Silenced | Spray and Pray |
| Assault Rifle | 2 | 2 | Far | Automatic | Silenced | — |
| Light Machine Gun | 2 | 3 | Far | Automatic | — | Spray and Pray, Covering Fire |
| Sniper Rifle | 3 | 2 | Very Far | Scoped | Collapsable, Silenced | Exploit Vulnerability |
| Rocket Launcher | 3 | 3 | Very Far | Consumable, Explosive, Spread | — | — |

---

## Thrown / Explosive

| Weapon | Damage | Load | Range | Tags | Weapon Moves |
|---|---|---|---|---|---|
| Flashbang | — | — | Nearby | Consumable | Confuse Senses |
| Grenade | 2 | 1 | Nearby | Explosive, Spread, Throwable | — |
