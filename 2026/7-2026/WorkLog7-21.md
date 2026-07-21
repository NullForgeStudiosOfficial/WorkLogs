
# Development Log — July 20, 2026

Today's work ended up becoming much larger than expected. While several new DLLs were designed, the biggest accomplishment wasn't creating mechanics—it was finally understanding the philosophies behind several of Daemon Protocol's realms. Those philosophies now naturally guide future ability design instead of every DLL needing to invent its own identity from scratch.

## Combat Grid Finalized

After experimenting with larger combat boards, the battlefield has been finalized at **15x15**.

This size strikes a good balance between readability and tactical depth. Larger boards became difficult to read inside Discord without zooming, while 15x15 still leaves enough room for meaningful positioning.

An added benefit is that it follows the "Rule of Threes." A 15 tile board naturally gives players **5 spaces of movement**, which feels like a comfortable default movement distance.

The previous idea of Ashbound using a different board size has been abandoned. Maintaining one consistent combat system across the project is simpler for both development and players.

---

## The Void Realm Finally Found Its Identity

One of the biggest design breakthroughs today was finally answering the question:

**What actually is the Void realm?**

Previously, Void was slowly becoming a collection of random "glitch" mechanics. That direction never felt satisfying.

Instead, Void has now become the realm of **exceptions.**

Void doesn't become stronger.

Void doesn't cast strange magic.

Void simply ignores assumptions everyone else believes are absolute.

That single realization immediately gave Void a cohesive design philosophy and made future DLL ideas much easier to evaluate.

---

## Mana Philosophy

One of the biggest worldbuilding decisions made today was redefining what mana actually represents inside Daemon Protocol.

The conclusion is simple:

**Mana powers abilities—not traditional spells.**

There are no generic damage spells.

No Fireball.

No Ice Spear.

No Lightning Bolt.

At first this felt unusual, but once viewed through the lens of Icolass, it immediately made sense.

Daemon Protocol takes place inside a civilization of machines.

Swinging a sword doesn't require mana.

Performing something physically impossible does.

Guardian protocols.

Reviving allies.

Corrupting yourself.

Entering Delirium.

Those consume system resources.

Mana therefore functions much more like computational or operational energy than mystical spellcasting.

---

## Vidulyn Philosophy

The mana discussion naturally evolved into one of the largest pieces of Vidulyn lore so far.

Vidulyn isn't simply "the metal realm."

It is literally a civilization that evolved inside machines.

Because of that, Vidulyn doesn't reject magic.

It rejects **imprecision.**

Raw spellcasting is viewed as messy, unpredictable, and difficult to control.

If a sword solves the problem...

Use the sword.

If reality itself must be manipulated...

Use mana.

This also completely redefines catalysts.

Catalysts are not wizard staffs.

They are engineered devices designed to safely manipulate mana.

They don't create magic.

They direct it.

This distinction makes mana feel much less like fantasy spellcasting and much more like engineering.

---

## Catalyst Critical Hits

An unexpected piece of lore emerged from this discussion.

Catalysts have always exploded on critical hits mechanically.

Now that mechanic finally has an in-universe explanation.

During normal operation, catalysts remain within engineered tolerances.

Critical hits represent an unexpected resonance that exceeds those tolerances.

To the player, it's simply a critical hit.

To a Vidulyn engineer, it's catastrophic equipment failure caused by exceeding design specifications.

This also reinforces why Vidulyn relies on engineered tools instead of casually manipulating raw mana.

---

## Overall Design Philosophy

Today's discussions reinforced something that has become increasingly obvious during development.

Traditional RPG progression often relies on simple statistical bonuses.

+10% Damage.

+10% Defense.

+5% Critical Chance.

All games in Ardron Universe almost never follow that approach.

Instead, its mechanics are designed to fundamentally change how encounters are played.

A single DLL choices in Daemon Protocol should change how you view the game as a whole, and give you many options to play with, or at least exceed at.

These mechanics naturally interact with terrain, equipment, creatures, bosses, and future systems.

That interaction significantly increases development time, but it also creates memorable gameplay rather than forgettable percentages.

Players rarely remember a +10% damage bonus.

They remember the battle where the battlefield caught fire, the Void player ignored half the game's assumptions, and the boss lost because the party couldn't miss.

Today's work reinforced that this philosophy is worth preserving despite the additional implementation effort.

---

## Ending Thought

The biggest achievement today wasn't creating several new DLLs.

It was finally understanding that the realms are no longer simply collections of mechanics.

They are cultures with their own philosophies.

Void represents exceptions.

Vidulyn represents engineering and precision.

Sostrum weaponizes the battlefield itself.

Grimlowe embraces sacrifice in pursuit of power.

With those identities established, future DLL design should become significantly more natural because mechanics can now grow directly from each realm's worldview instead of being invented independently every time.


---

This was the first half of my work. I will make another log below. 

---

## NullForge Website & Companion Portal

A significant portion of today's work shifted away from gameplay systems and toward creating a website for NullForge Studios.

The original goal was straightforward: build a central landing page that connected every major Ardron Universe project, including Daemon Protocol, the Realm Quiz, Discord, development logs, and community resources.

By the end of development, the site had evolved into a polished desktop experience featuring animated CRT effects, custom card layouts, layered backgrounds, and interactive navigation between every major project.

Unexpectedly, the website also became an opportunity to learn an entirely new area of software development.

Throughout the process, numerous frontend problems had to be solved involving HTML structure, CSS styling, JavaScript interactions, animations, responsive layouts, and browser behavior. Although these technologies were unfamiliar at first, the overall debugging process proved remarkably similar to every other language used throughout the project: identify assumptions, verify behavior, isolate the incorrect variable, and correct it.

One major conclusion became increasingly obvious during development:

**NullForge is fundamentally a desktop-first ecosystem.**

Supporting mobile devices introduced a disproportionate amount of complexity while offering relatively little value for the type of experience Daemon Protocol is intended to provide.

This realization also changed how the Companion Portal is viewed.

Rather than behaving like a traditional website, it has gradually evolved into a full management application containing character creation, equipment management, DLL browsing, lore databases, and future player utilities.

Because of this, there is now serious consideration toward eventually moving much of the Companion Portal into the Unity client. Doing so would allow the interface to share the same development environment, UI philosophy, and tooling already used throughout Ardron Universe while avoiding many of the limitations imposed by browser-based applications.

Regardless of where those systems ultimately reside, the website itself represents an important milestone.

It successfully established a professional public presence for NullForge Studios while simultaneously expanding the project's technical foundation through practical experience with HTML, CSS, JavaScript, and frontend development as a whole.

---

P.S
Work time from NullFocus won't be accurate, As alot of web development took place with Firefox. It recorded 4 hours, and 46 minutes of time. How much of that was liesure/dev I can't be sure. So it is not included.