---
status: draft
---

# Weapons

Each weapon has the following stats:

- **Damage** — how much harm it deals on a hit
- **Ammo** — shots before reload (ranged weapons only)
- **Load** — encumbrance cost to carry
- **Range** — Next to / Nearby / Far / Very Far
- **Tags** — passive properties that change how the weapon works (see `weapon-tags.md`)
- **Modifications** — optional upgrades that can be added to the weapon
- **Weapon Moves** — special actions available only with this weapon (see `weapon-moves.md`)

---

## Melee Weapons

| Weapon | Damage | Load | Range | Tags | Modifications | Weapon Moves |
|---|---|---|---|---|---|---|
| Baton | 1 | 2 | Next to | Non-lethal | — | — |
| Dagger | 1 | 1 | Next to | Sneaky, Throwable | Concealable, Counterweighted, Electrified, Magnetic, Multi-tool, Tethered, Throw-balanced | Exploit Vulnerability |
| Hammer | 2 | 2 | Next to | — | — | Wreck |
| Rapier | 2 | 2 | Next to | — | Hidden | Disarming Strike, Parry |
| Spear | 2 | 2 | Next to | Throwable | Collapsable, Electrified, Throw-balanced | — |
| Sword | 2 | 2 | Next to | Cleave | Counterweighted, Throw-balanced | Parry, Cleave |

---

## Ranged Weapons

| Weapon | Damage | Ammo | Load | Range | Tags | Modifications | Weapon Moves |
|---|---|---|---|---|---|---|---|
| Pistol | 1 | 4 | 1 | Nearby | — | Concealable, Silenced | Double Tap, Quickdraw, Disarming Shot |
| Shotgun | 2 | 3 | 2 | Nearby | Spread | — | Spread, Wreck |
| Sub-machine Gun | 2 | 5 | 2 | Nearby | Automatic | Collapsable, Silenced | Spray and Pray |
| Assault Rifle | 2 | 4 | 2 | Far | Automatic | Silenced | Burst Fire |
| Light Machine Gun | 2 | 6 | 3 | Far | Automatic | — | Spray and Pray, Covering Fire, Burst Fire |
| Sniper Rifle | 3 | 3 | 2 | Very Far | Scoped | Collapsable, Silenced | Exploit Vulnerability |
| Rocket Launcher | 3 | 2 | 3 | Very Far | Consumable, Explosive, Spread | — | — |

---

## Thrown / Explosive

| Weapon | Damage | Ammo | Load | Range | Tags | Weapon Moves |
|---|---|---|---|---|---|---|
| Flashbang | — | — | — | Nearby | Consumable | Confuse Senses |
| Grenade | 2 | 1 | 1 | Nearby | Explosive, Spread, Throwable | — |
