# KingsTweaks

A quality-of-life mod for Valheim.

Every feature can be turned on or off, and the server's settings are enforced on all connected players automatically without losing your singleplayer or personal config.

Editing the config file on a running server applies the changes live and pushes them to everyone; most changes require no restart. Admins can also edit settings from an in-game menu.

---

## Structures

- Structures don't decay from rain, even without a roof.
- Optional protection from water damage (waves, tides, flooded ground).
- Optional: only protect structures inside an active ward, so abandoned builds still decay.
- No stamina cost for building, deconstructing, hoeing and planting inside a ward.
- Optional **build anywhere**: removes the no-build zones in caves, crypts, dungeons and around boss altars.

## Wards

- Adjustable ward radius.
- Creatures don't spawn inside an active ward, so mobs stop appearing in your base.

## Fires and torches

- Optional infinite fuel, with separate toggles for torches, campfires and other fires. Off by default.

## Buildable chests

- **Fuel Chest** — stock it with wood, resin or any other fire fuel. Once a day it refills every fire and torch in range, each with its correct fuel type. Burned-out fires relight automatically.
- **Item Collector** — automatically pulls in dropped items within range. Only takes items that have been on the ground for 5 minutes (configurable), so it never grabs items right after they're dropped.
- **Trash Can** — anything left inside is permanently deleted when you close it.
- **Upkeep Chest** — once a day it repairs every damaged structure in range, paying a share of each piece's own build materials from the chest. The cost multiplier is configurable, and 0 makes repairs free.
- **Sorter Chest** — pushes whatever you put inside into nearby chests that already hold the same item, moving what fits when a chest is full and telling you what has nowhere to go.
- **Smelter Chest** — feeds ore and fuel to smelters, kilns, furnaces and blast furnaces in range, and collects what they produce.
- **Trough** — tame animals eat from it instead of being hand-fed. It only puts out food the animals in range actually eat, and only when they're hungry.

## Crafting and storage

- **Craft from chests:** building and crafting can use items stored in nearby chests as well as your inventory. Your inventory items are used first.
- **Shared chests:** more than one player can have the same chest open at once.

## Portal Hubs

A buildable portal that travels to any other hub linked to it.

- Name a hub with the normal portal name box; names are unique across the world.
- Walk into a hub to open its destination list; press Use to manage links. Step away and the list closes.
- Link destinations by name, so nobody can travel to a hub they weren't given.
- Links to hubs that no longer exist are removed automatically.
- Hubs you build are pinned on your map automatically.
- `/myhubs` lists the hubs you built, and `/linkall` links all of them to the hub you're standing at.

## Portals

- Adjustable range at which portals light up and activate.
- Optional **teleport everything**: ore, metal bars and anything else normally blocked can go through portals.

## Boats

- Set a custom max health for each boat type: Raft, Karve, Longship and Drakkar.
- Deconstruct boats with the hammer to get your materials back.
- Boats you build get a map marker that follows them, using the boat's own icon, and disappears when the boat does.
- **Experimental:** build on boats. Pieces placed while standing on a boat attach to it and sail with it.

## Tames

- Tame animals standing on a boat stay put instead of wandering off or jumping into deep water.
- Press a key on a tame near a boat to put it on board; press again to take it off onto dry land.
- Tames following you come through portals and Portal Hubs with you.
- Adjustable health for tamed animals, either one multiplier for everything or per species, e.g. `Boar:2, Wolf:4`. Wild animals are untouched.

## Planting

- Berry bushes, mushrooms, thistle and dandelions can be planted with the cultivator and grow over time.
- No spacing rule: crops never say they need more room to grow, so you can plant them right next to each other.

## Combat

- Your shield is drawn automatically when you equip a one-handed weapon, bringing back whichever shield you last carried. Toggle with `/autoshield`.

## Beds and doors

- **Beds:** tap E on an unclaimed bed to sleep in it without claiming it or changing your spawn point. Hold E to claim it normally and set your spawn.
- **Doors:** tap E to open a door away from you, hold E to open it towards you.

## World and comfort

- Separate multipliers for how long, or short, days and nights last.
- Comfort pieces count from farther away (20 m by default instead of 10 m), so big halls reach higher comfort levels.

## Dropped items

- Items float on the water surface instead of sinking.
- Nearby dropped items of the same type merge into one stack, reducing clutter and improving server performance.

## Interface

- **Compass** across the top of the screen, showing headings plus your map pins with their icons and distances. Pins you've crossed out on the map are left off, and it hides while the full map is open. Toggle with `/compass`.
- **First person:** zoom all the way in and the camera moves to your eyes. Zoom back out for the normal view.
- **First run hint:** the first time you play, a message tells you which key opens the settings. Only shown to players who can actually change them.
- **In-game settings menu** on the Home key. Admins can change any setting live; everyone else sees the server's values.
- **Activity feed:** short messages on the left when your chests do something. Toggle with `/uinotifications`.
- **Mist clearing:** `/mist` clears the Mistlands fog around you, with an adjustable radius. Admins can disable it server-wide.
- Optional: hide Yggdrasil, the giant tree in the sky.

## Chat

- Chat is server-wide by default instead of local, with a key to switch between the two.
- Shouted messages and pings stay in the chat window instead of appearing above players' heads.
- Death notifications in server chat, saying what killed you and the biome you died in, e.g. "was killed by a Greydwarf in the Black Forest".
- Message of the day, shown once when a player joins.

## Commands

- `/help` — lists every KingsTweaks command.
- `/unstuck` — moves you to solid ground nearby. Can be disabled server-side, with a cooldown.
- `/myhubs` — lists the Portal Hubs you built, with coordinates.
- `/linkall` — links every hub you built to the hub you're standing at.
- `/mist` — clears or restores the Mistlands fog around you.
- `/compass` — turns the compass strip on or off.
- `/autoshield` — draws your shield automatically with a one-handed weapon.
- `/uinotifications` — turns the corner activity messages on or off.

## Server settings worth knowing

- **Map off:** a server can take the minimap and the full map away from everyone.
- **Compass off:** a server can disable the compass for everyone, whatever each player has chosen.
- **Mist clearing** can be disabled server-wide, and so can `/unstuck`.
- Personal choices such as the compass, activity feed and auto-shield are kept per player and are never overwritten by the server.

## Server tools

- **Server password saver:** the password you enter when joining a server is saved and entered automatically next time. If it changes, you're prompted for the new one.
- **Continue button** on the main menu, loading whatever you played last: the same character plus either that world or that server.
- **World backups:** after the game saves, the world files are copied into a backups folder, keeping as many as you choose and deleting the oldest.
- **Version enforcement:** players must run the same KingsTweaks version to join. Anyone without the mod is disconnected.

---

## Installation

Requires BepInEx.

1. Install `KingsTweaks.dll` in `BepInEx/plugins` on the server and on each client.
2. Launch the game once. The config file is created at `BepInEx/config/dev.craz.kingstweaks.cfg`.

Updating is safe: if a release moves settings into different sections, your existing values are carried across to the new layout automatically. Your own display preferences live in a separate file, so a server never overwrites them.
