
# Development Log — July 20, 2026

Today's work focused almost entirely on refining Daemon Protocol's combat systems. The biggest theme was validating interactions between mechanics rather than adding entirely new features.

## Catalyst Combat

The catalyst weapon family received the most attention.

The original concern was that cone attacks divide their damage between all hostile targets, resulting in extremely low per-target damage against groups. This raised concerns that weaker catalysts (such as the Focus Ring) could become ineffective once Ward and magical mitigation were applied.

Rather than immediately increasing catalyst damage across the board, the discussion shifted toward the overall action economy.

Catalysts consume Quick Action Points (QAP), allowing multiple casts within a single round before consuming normal AP. This reframed catalyst balance around **damage per round** instead of **damage per cast**.

The Focus Ring now represents a rapid-fire magical weapon rather than a heavy spellcaster's implement.

## Multi-Attack Commands

A quality-of-life improvement was designed for QAP weapons.

Instead of repeatedly issuing attack commands, weapons capable of multiple attacks can simply specify the number of attacks:

```
!attack left 6
```

The combat engine performs the attacks internally while producing a single combat log, significantly reducing command spam.

## Unstoppable Force DLL

A new Grimlowe DLL was created:

**Unstoppable Force**

> Whenever you hit a creature two or more times in the same round, your second and subsequent successful hits against that creature ignore its Defense and Impedance.

This DLL naturally rewards rapid-fire weapons without modifying the underlying combat formulas.

An important realization followed:

The mechanic tracks **successful hits per target**, not consecutive attacks.

Example:

* Hit Target A
* Hit Target A
* Miss Target A
* Hit Target A

The final hit still ignores Defense because Target A has already been struck multiple times during the round.

Each target independently builds its own "pressure."

## Weapon Balance

Several ranged weapons were reviewed:

* Recurve Bow
* Crossbow
* Sling
* Musket
* Pistol
* Rifle
* Pump Shotgun

While evaluating possible exploits involving rapid-fire pistols and armor bypass, multiple systems were found to naturally prevent abuse.

Key balancing factors include:

* AP/QAP economy
* Reload requirements
* Magazine sizes
* Two-handed weapon restrictions
* Pre-combat equipment selection

Several suspected exploits ultimately disappeared once these systems were considered together.

## Combat Restrictions

One important realization was that equipment cannot be changed during combat.

Weapon swapping is handled through inventory commands, and inventory commands are ignored while in battle.

This prevents a variety of theoretical exploits without introducing additional special-case rules.

Examples prevented automatically include:

* Building armor-penetration stacks with one weapon before switching to a high-damage weapon.
* Swapping equipment in response to enemy damage types.
* Mid-combat inventory abuse.

This reinforced confidence in the existing combat architecture rather than requiring additional restrictions.

## Overall

Today's work wasn't about adding large amounts of content. Instead, it was spent pressure-testing the combat engine.

Several interactions initially appeared exploitable, but nearly every concern was already mitigated by systems implemented earlier, including AP costs, reload mechanics, two-handed weapon restrictions, and combat inventory locking.

This is a good indication that the combat systems are beginning to reinforce one another instead of requiring new rules for every edge case.

-------------------
## Ending Thought

It was supposed to be my day off, and it was for a majority of that time, but Ardron waits for no one.