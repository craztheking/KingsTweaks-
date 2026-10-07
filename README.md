# KingsTweaks

An all-in-one quality-of-life mod for Valheim, for both servers and single player.

Install it on a server and every connected player gets the same rules, enforced automatically. Install it on your own game and it works exactly the same way on your own worlds.

Every feature can be turned on or off, and your own display preferences stay yours on any server.

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
- A server can take ordinary portals out of the build menu entirely, leaving Portal Hubs as the only way to travel.

## Boats

- Set a custom max health for each boat type: Raft, Karve, Longship and Drakkar.
- Deconstruct boats with the hammer to get your materials back.
- Boats you build get a map marker that follows them, using the boat's own icon, and disappears when the boat does.
- **Experimental:** build on boats. Pieces placed while standing on a boat attach to it and sail with it.

## Tames

- Tame animals standing on a boat stay put instead of wandering off or jumping into deep water.
- Press a key on a tame near a boat to put it on board; press again to take it off onto dry land.
- Tames following you come through portals and Portal Hubs with you.
- Hold your stow key on a tame to track it on the map; the marker follows it. Hold again to stop.
- Adjustable health for tamed animals, either one multiplier for everything or per species, e.g. `Boar:2, Wolf:4`. Wild animals are untouched, and each animal remembers its original health so changing the multiplier always scales from that.

## Planting

- Berry bushes, mushrooms, thistle and dandelions can be planted with the cultivator and grow over time.
- No spacing rule: crops never say they need more room to grow, so you can plant them right next to each other.

## Teams

- Create a team from the **Team** button on the pause menu, or with `/team`.
- Look at another player and hold your stow key to invite them; they accept or decline from the same window.
- **Ranks:** whoever makes the team leads it. The leader can promote members to officer, demote them, remove anyone, and hand the team over. Officers can invite and remove ordinary members. If the leader leaves, an officer takes over.
- **Team chat** with `/t your message`.
- **Map pings** are only seen by your own team. Players with no team see pings as normal.
- **A health list** under the minimap, showing each team mate and how they're doing, with no panel in the way.
- **Wards let your team through** without adding anyone by hand.
- Teams and ranks survive restarts.

## Travel

- `/sethome` and `/home` remember a spot and take you back to it.
- `/tpr <player>` asks if you can travel to them; `/tphere <player>` asks them to come to you. They accept with `/tpa` (or `/tpaccept`) and refuse with `/tpdeny`.
- A countdown before you arrive, cancelled if you're hit, plus a cooldown between journeys.
- Travel is refused for a while after you've taken damage and while an enemy is close by. All of it is configurable, and a server can turn the whole thing off.

## Combat

- Your shield is drawn automatically when you equip a one-handed weapon, bringing back whichever shield you last carried. Toggle with `/autoshield`.
- **Guardian power resets when you die**, so you respawn ready instead of carrying a cooldown through death.

## Beds and doors

- **Beds:** tap E on an unclaimed bed to sleep in it without claiming it or changing your spawn point. Hold E to claim it normally and set your spawn.
- **Doors:** tap E to open a door away from you, hold E to open it towards you. Doors still work with the hammer out.
- **Door locks:** press your stow key on a door inside your ward to lock it. A locked door only opens for people the ward permits, and the lock stays put across sessions.
- **Chests:** hold E on a chest to give it a name.

## Signs

- Signs hold more text than the game normally allows — 150 characters by default, adjustable. Long text still has to fit on the sign, so it gets small.

## Locks

- Press your stow key on a door, a chest or a ward to lock it.
- A locked thing only opens for people the ward permits; everyone else is told it's locked.
- Doors and chests have to be inside a ward to be locked. A ward is its own authority, so locking one stops anyone it doesn't permit switching it off or editing its list.
- Locks live on the object, so they hold across sessions and apply to every player.

## World and comfort

- Separate multipliers for how long, or short, days and nights last.
- Comfort pieces count from farther away (20 m by default instead of 10 m), so big halls reach higher comfort levels.

## Map

- **Exploration multiplier:** choose how much of the map you uncover as you travel. 2 reveals twice as far as normal, 0.5 half as far. Map you already have stays as it is.

## Dropped items

- Items float on the water surface instead of sinking.
- Nearby dropped items of the same type merge into one stack, reducing clutter and improving server performance.
- Collectors only take loose items: anything placed on a table, a stand or a build piece is left alone.

## Interface

- **Compass** across the top of the screen, showing headings plus your map pins with their icons and distances. Pins you've crossed out on the map are left off, and it hides while the full map is open. Toggle with `/compass`.
- **First person:** zoom all the way in and the camera moves to your eyes; zoom back out for the normal view. Your body faces where you look, so you can walk backwards without turning around. The camera follows your head, so it ducks when you crouch and sit, and head bob can be turned off. Every camera setting can be adjusted from the in-game menu and applies instantly, so you can find your preferred view while looking at it. Servers can disable first person or require it.
- **First run hint:** the first time you play, a message tells you which key opens the settings. Only shown to players who can actually change them.
- **In-game settings menu** on the Home key. Admins can change any setting live, and every player can change their own settings there even on someone else's server.
- **Activity feed:** short messages on the left when your chests do something. Toggle with `/uinotifications`.
- **Mist clearing:** `/mist` clears the Mistlands fog around you, with an adjustable radius. Admins can disable it server-wide.
- Optional: hide Yggdrasil, the giant tree in the sky.

## Appearance

- `/dye #aa3344` colours the item in your first hotbar slot, and `/dye 3 black` colours slot 3 instead. Named colours work as well as hex: red, blue, green, purple, pink, black, white and others.
- `/dye clear` puts an item back to normal.
- The colour lives on the item, so it survives dropping, trading and relogging, and everyone else sees it too.

## Chat

- Chat is server-wide by default instead of local, with a key to switch between the two.
- Shouted messages stay in the chat window instead of appearing above players' heads, and shouts are shown as typed rather than IN CAPITALS.
- Death notifications in server chat, saying what killed you and the biome you died in, e.g. "was killed by a Greydwarf in the Black Forest".
- Message of the day, shown once when a player joins.

## Commands

- `/kt` — lists every KingsTweaks command. The game's own `/help` lists everything else.
- `/unstuck` — moves you to solid ground nearby. Can be disabled server-side, with a cooldown.
- `/myhubs` — lists the Portal Hubs you built, with coordinates.
- `/linkall` — links every hub you built to the hub you're standing at.
- `/mist` — clears or restores the Mistlands fog around you.
- `/compass` — turns the compass strip on or off.
- `/autoshield` — draws your shield automatically with a one-handed weapon.
- `/team` — opens the team window.
- `/t <message>` — sends a message to your team.
- `/dye <colour>` — colours the item in your first slot. `/dye 3 black` colours slot 3 instead.
- `/teamkick`, `/teampromote`, `/teamdemote`, `/teamleader` — manage your team.
- `/fpparts` — lists the parts of your character, for the first person hide list.
- `/uinotifications` — turns the corner activity messages on or off.
- `/who` — lists everyone online. A server can limit this to admins.
- `/playtime` — your time on the server, or `/playtime <player>` for someone else's.

**Admin only**

- `/admin <name or Steam64 ID>` — makes a player an admin; `/removeadmin` takes it away. A name works for anyone currently online.
- `/tp <player>` — takes you straight to them.
- `/heal` — fills your health, stamina and eitr.
- `/repair` — mends everything you're carrying.
- `/freebuild` — build without paying for materials.

## Repair

- Standing at a workbench or forge repairs everything you're carrying that the station could repair by hand.

## Server settings worth knowing

- **Map off:** the minimap and the full map can each be taken away from everyone, separately, and switched back on without a restart.
- **Map exploration:** how much of the world each player uncovers as they travel.
- **Compass off:** a server can disable the compass for everyone, whatever each player has chosen.
- **First person off or forced:** a server can take first person away, or require it for everyone.
- **Mist clearing** can be disabled server-wide, and so can `/unstuck`.
- **Ward respect:** the Fuel, Upkeep and craft-from-chests features ignore anything inside a ward the owner isn't permitted on.
- **Forced PvP:** everyone is flagged and can't switch it off.
- **Spawn scaling:** hostile creatures and passive animals can be multiplied separately, from a quarter to ten times.
- **No portals:** ordinary portals can be removed from the build menu, leaving Portal Hubs as the only travel.
- **Hub travel cost:** each hub journey can cost an item, set in the config.
- **`/who` for admins only**, if you'd rather players couldn't see who's online.
- Personal choices such as the compass, activity feed, auto-shield and camera placement are kept per player and are never overwritten by the server. Players can change those from the in-game menu even on a server they don't administer.

## Server tools

- **Server password saver:** the password you enter when joining a server is saved and entered automatically next time. If it changes, you're prompted for the new one.
- **Continue button** on the main menu, loading whatever you played last: the same character plus either that world or that server.
- **World backups:** after the game saves, the world files are copied into a backups folder, keeping as many as you choose and deleting the oldest.
- **Scheduled restarts:** at times you set, everyone is warned in chat, the world is saved and the server closes. Starting it again is up to your start script or service, since a game can't relaunch itself.
- **Playtime tracking** per player, surviving restarts, readable with `/playtime`.
- **Version enforcement:** players must run the same KingsTweaks version to join. Anyone without the mod is disconnected.

---

## Installation

Requires BepInEx.

1. Install `KingsTweaks.dll` in `BepInEx/plugins` on the server and on each client.
2. Launch the game once. The config file is created at `BepInEx/config/dev.craz.kingstweaks.cfg`.

Updating is safe: if a release moves settings into different sections, your existing values are carried across to the new layout automatically. Your own display preferences live in a separate file, so a server never overwrites them.
