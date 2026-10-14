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
- **Carts come apart with the hammer**, giving their materials back. A cart with anything in it has to be emptied first, so nothing is destroyed with it.
- **Workstation upgrades place freely:** anvils, the adze, tool shelf, forge cooler, chopping block and the rest no longer ask for more space, so they can sit side by side or against a wall. Their distance from the station is adjustable too — 10 m by default instead of the game's 5.
- Optional **build anywhere**: removes the no-build zones in caves, crypts, dungeons and around boss altars.

## Wards

- Adjustable ward radius.
- Creatures don't spawn inside an active ward, so mobs stop appearing in your base.

## Fires and torches

- Optional infinite fuel, with separate toggles for torches, campfires and other fires. Off by default.

## Buildable chests

- **Fuel Chest** — stock it with wood, resin or any other fire fuel. Once a day it refills every fire and torch in range, each with its correct fuel type. Burned-out fires relight automatically. If it runs short it says what to put in — "Needs 24 Wood, 6 Resin" on the chest itself, so anyone walking past can top it up.
- **Item Collector** — automatically pulls in dropped items within range. Only takes items that have been on the ground for 5 minutes (configurable), so it never grabs items right after they're dropped.
- **Trash Can** — anything left inside is permanently deleted when you close it.
- **Upkeep Chest** — once a day it repairs every damaged structure in range, paying a share of each piece's own build materials from the chest. The cost multiplier is configurable, and 0 makes repairs free.
- **Sorter Chest** — pushes whatever you put inside into nearby chests that already hold the same item. It names where things went — "20 Stone to \"ores\"" — moves what fits when a chest is full, and tells you what has nowhere to go.
- **Smelter Chest** — feeds ore and fuel to smelters, kilns, furnaces and blast furnaces in range, and collects what they produce.
- **Trough** — tame animals eat from it instead of being hand-fed. It only puts out food the animals in range actually eat, and only when they're hungry, and it tosses each item towards the animal rather than dropping it on the trough.

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
- **Creatures leave empty boats alone.** A boat with nobody aboard can't be damaged by wildlife, so a serpent doesn't eat the longship you left at the dock. Players can still break it, and a boat somebody is standing on is fair game as usual.

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
- **Team mates on your map**, whether or not they've switched their own map sharing on. Only the team sees them, so nobody is announced to the rest of the server.
- **A team list** under the minimap: each mate's name, a health bar with the real numbers, an arrow pointing the way to them and how far off they are. The arrow turns with you, so it points where to walk; the letter after the distance is the compass direction. Names are coloured by rank, and only mates who are actually online are listed.
- **Wards let your team through** without adding anyone by hand.
- Teams and ranks survive restarts.

## Travel

- `/sethome` and `/home` remember a spot and take you back to it.
- `/tpr <player>` asks if you can travel to them; `/tphere <player>` asks them to come to you. They accept with `/tpa` (or `/tpaccept`) and refuse with `/tpdeny`.
- A countdown before you arrive, cancelled if you're hit, plus a cooldown between journeys.
- Travel is refused for a while after you've taken damage and while an enemy is close by. All of it is configurable, and a server can turn the whole thing off.
- **Not while over-encumbered:** a full load has to be carried or sailed home. Checked again at the moment you arrive, so you can't load up during the countdown.
- **Metals:** by default the travel commands won't carry ore, bars or anything else a portal refuses. This is a separate setting from the portal one, so a server can let portals take metal while `/home` still can't.
- **Server warps:** an admin stands somewhere and runs `/addtp trader 300` to make `/trader` available to everyone, with a five minute wait between uses. `/tplist` shows what a server offers. Warps use the same countdown and combat rules as everything else, so they aren't an escape hatch.

## Combat

- **Thrown spears come back to you** instead of being left where they landed. A spear you deliberately drop on the ground stays dropped.
- **Your torch stays lit** when you take out the hammer, hoe or cultivator, so building at night isn't done in the dark.
- Optional: **no skill loss on death**. Off by default.
- Your shield is drawn automatically when you equip a one-handed weapon, bringing back whichever shield you last carried. Toggle with `/autoshield`.
- **Guardian power resets when you die**, so you respawn ready instead of carrying a cooldown through death.

## Beds and doors

- **Beds:** tap E on an unclaimed bed to sleep in it without claiming it or changing your spawn point. Hold E to claim it normally and set your spawn.
- **Doors:** tap E to open a door away from you, hold E to open it towards you. Doors still work with the hammer out.
- **Door locks:** tap your stow key on a door inside your ward to lock it. A locked door only opens for people the ward permits, and the lock stays put across sessions.
- **Chests:** tap your stow key on a chest to lock it, hold it to give it a name.

## Signs

- Signs hold more text than the game normally allows — 150 characters by default, adjustable. Long text still has to fit on the sign, so it gets small.

## Locks

- Tap your stow key on a door, a chest or a ward to lock it. Holding it on a chest renames the chest instead.
- A locked thing only opens for people the ward permits; everyone else is told it's locked.
- Doors and chests have to be inside a ward to be locked. A ward is its own authority, so locking one stops anyone it doesn't permit switching it off or editing its list.
- Locks live on the object, so they hold across sessions and apply to every player.

## World and comfort

- **No tree stumps:** optionally, felling a tree leaves nothing behind to chop a second time. The stump still gives up its wood, so nothing is lost. Off by default. Only trees cut down while it's on are affected — stumps already standing in your world, and the ones that are part of the landscape, are left alone.
- Separate multipliers for how long, or short, days and nights last.
- Comfort pieces count from farther away (20 m by default instead of 10 m), so big halls reach higher comfort levels.

## Map

- **Cartography tables share the map, not your pins.** The exploration passes between players as usual; nobody hands over their base, portals and stashes by accident.
- Optional: hide the **"Day 12"** message each morning. Off by default, and each player's own choice.
- **Clear death markers:** a button on the full map removes every death marker at once, instead of right-clicking them one at a time.
- **Exploration multiplier:** choose how much of the map you uncover as you travel. 2 reveals twice as far as normal, 0.5 half as far. Map you already have stays as it is.

## Dropped items

- Items float on the water surface instead of sinking.
- Nearby dropped items of the same type merge into one stack, reducing clutter and improving server performance.
- Collectors only take loose items: anything placed on a table, a stand or a build piece is left alone.

## Interface

- **Compass** across the top of the screen, showing headings plus your map pins with their icons and distances. Pins you've crossed out on the map are left off, and it hides while the full map is open. Toggle with `/compass`.
- **First person:** zoom all the way in and the camera moves to your eyes; zoom back out for the normal view. Your body faces where you look, so you can walk backwards without turning around. The camera follows your head, so it ducks when you crouch and sit, and head bob can be turned off. Every camera setting can be adjusted from the in-game menu and applies instantly, so you can find your preferred view while looking at it. Servers can disable first person or require it.
- **First run hint:** the first time you play, a message tells you which key opens the settings. Only shown to players who can actually change them.
- **In-game settings menu** on the Home key, with a row of tabs across the top. **Server** holds the rules everyone plays by; **Client** holds the display and comfort choices that follow you from server to server. Admins can change any setting live, and every player can change their own even on someone else's server. Six more tabs sit beside those two — see the admin panel below; the Players one is shown to everybody.
- **Activity feed:** short messages on the left when your chests do something. A chest that keeps being short of something says so once when you come to it and then only every few minutes, instead of every few seconds. Toggle with `/uinotifications`.
- **Mist clearing:** `/mist` clears the Mistlands fog around you, with an adjustable radius. Admins can disable it server-wide.
- **Fog and embers:** `/fog` turns off the biome fog — the Plains haze, the Deep North whiteout, the murk over the Ashlands — and `/ember` stops the falling ash and embers. Both are yours alone: nobody else's view changes, and each can be set to start that way or be disabled server-wide. `/mist` still handles the Mistlands, which the game clears a different way.
- **Nothing fires while you're typing.** None of the keys this mod watches do anything in chat, on a sign, in the inventory or in a menu, so writing a message never locks a chest or opens a door behind you.
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

Commands work however they're typed — `/Home` and `/HOME` do the same as `/home`. That applies to the game's own commands too, not just these.

- `/kt` — lists every KingsTweaks command. The game's own `/help` lists everything else.
- `/spectate <name>` — watches a player, and again to stop.
- `/find <text>` — narrows the crafting list.
- `/size <number>` — changes how big your character is.
- `/ktcheck` — checks every part of the game this mod reaches into by name and prints what it found. Anything marked MISSING is a feature that can't work on your build. Worth running first whenever something "used to work".
- `/unstuck` — moves you to solid ground nearby. Can be disabled server-side, with a cooldown.
- `/fog` — turns the biome fog off for you only.
- `/ember` — stops the falling ash and embers for you only.
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
- `/who` — lists everyone online, with how long each of them has been on the server. A server can limit this to admins.
- `/playtime` — your time on the server, or `/playtime <player>` for someone else's.
- `/tplist` — lists the warps this server offers.
- `/sethome`, `/home`, `/tpr <player>`, `/tphere <player>`, `/tpa`, `/tpdeny` — see **Travel** above.

**Admin only.** With permissions turned on, each of these needs the matching right rather than just being an admin.

- `/admin <name or Steam64 ID>` — makes a player an admin; `/removeadmin` takes it away. A name works for anyone currently online.
- `/tp <player>` — takes you straight to them.
- `/heal` — fills your health, stamina and eitr.
- `/repair` — mends everything you're carrying.
- `/freebuild` — build without paying for materials.
- `/addtp <name> [seconds]` — makes where you stand into a warp everyone can use.
- `/deltp <name>` — removes a warp.
- `/sleeperpurge confirm` — removes every sleeping body in the world. It asks for the word `confirm` because without server characters a body holds its owner's inventory.

## Repair

- Standing at a workbench or forge repairs everything you're carrying that the station could repair by hand.

## Sleepers

*Off by default.*

- Log out and your character stays in the world, lying asleep where you left off, wearing what you were wearing and holding what you were holding.
- What's in the body **is** your inventory: whatever is still there when you return is what you get, so being robbed costs you something real.
- A body is only visible and lootable while its owner is offline. While you're playing, nobody can see or open yours.
- Creatures ignore sleeping bodies. Players can destroy them.
- Your body is kept up to date every few seconds while you play, so anything picked up in the last moments before you log out may not make it in.
- Dying empties your body: what you were carrying is in your tombstone, so there's nothing left behind to loot twice.
- `/sleeperpurge confirm` clears every body out of the world, for an admin who wants a clean slate.
- The body is a copy of the character model with everything that makes it a player taken off it, so it can't move, be hit or be mistaken for someone online. If a game version ever stops the copy being made, the body falls back to a plain chest rather than vanishing — `/ktcheck` says which it is.

## Server characters

*Off by default.*

- The server keeps each player's belongings and skills. The first time somebody joins, their inventory is emptied and their skills start at zero, so nothing can be carried in from another world.
- Joining shows a notice first. Until a player accepts it they can't move, open their inventory, be hurt, or leave a body behind — and nothing is wiped. There's a button to leave instead.
- Characters are stored against the player's platform ID, not their character name, so renaming doesn't pick up somebody else's things.
- Each world keeps its own store, so hosting two worlds from one install doesn't let a character cross between them.
- Looting somebody's sleeping body changes what the server is holding for them, so theft sticks even after a restart.
- This stops importing by anyone playing the game normally. It is not anti-cheat: Valheim keeps characters on each player's own machine, so a modified client could still lie. Version enforcement raises the bar without removing it.

## Server settings worth knowing

- **Map off:** the minimap and the full map can each be taken away from everyone, separately, and switched back on without a restart.
- **Map exploration:** how much of the world each player uncovers as they travel.
- **Compass off:** a server can disable the compass for everyone, whatever each player has chosen.
- **First person off or forced:** a server can take first person away, or require it for everyone.
- **Mist clearing** can be disabled server-wide, and so can `/unstuck`, `/fog` and `/ember`.
- **Ward respect:** the Fuel, Upkeep and craft-from-chests features ignore anything inside a ward the owner isn't permitted on.
- **Forced PvP:** everyone is flagged and can't switch it off.
- **Spawn scaling:** hostile creatures and passive animals can be multiplied separately, from a quarter to ten times.
- **No portals:** ordinary portals can be removed from the build menu, leaving Portal Hubs as the only travel.
- **Hub travel cost:** each hub journey can cost an item, set in the config.
- **Overlapping placement:** *off by default.* Pieces may be placed inside one another — a workstation inside a table, a chest under a stair. Everything else about placement is unchanged: being out of materials, standing too far away or building inside someone else's ward still refuses as usual.
- **Boats as workstations:** *off by default.* A boat carries a workbench, so gear can be repaired and pieces built while aboard without sailing home. It's a real copy of the workbench with the roof and fire requirements lifted, and its reach is configurable.
- **`/who` for admins only**, if you'd rather players couldn't see who's online.
- **Hide or disable commands:** keep chosen commands out of `/kt` and the game's `/help`, or refuse them outright so nobody can use them. The Commands tab of the admin panel does this with a switch per command.
- **Join message:** a line of your own shown to each player once when they arrive, with `{version}` replaced by the mod version. It ends with "Type /kt for all commands" so players find the command list without being told; that sentence can be switched off.
- Personal choices such as the compass, activity feed, auto-shield and camera placement are kept per player and are never overwritten by the server. Players can change those from the in-game menu even on a server they don't administer.

## Admin panel

Open the settings menu with Home and six more tabs sit beside the two settings pages. Everything on them is checked by the server before it happens — the buttons ask, the server decides. The Players tab is shown to everybody; the other five appear only for an admin, and only when that admin has a right the tab could use.

- **Players:** everyone online, with how long they've been on the server. Admins get a button each to kick, ban or make them an admin; banning asks you why, and the reason is kept. This one tab is shown to every player as a plain read-only list, since `/who` gives out the same thing — nobody else's buttons, and no platform IDs leave the server. It follows the `/who` settings, so a server that hides `/who` hides this too.
- **Bans:** everyone banned, with the reason and the date it was given, and a button to lift it. You can also ban somebody who isn't online by typing their Steam64 ID followed by the reason. Valheim has nowhere to record a reason, so KingsTweaks keeps them in a file of its own next to the config.
- **Allowed:** the server's allowed list, with a button to remove a name and a box to add one. While the list is empty anybody may join; adding a single name shuts out everybody else, and the page says so.
- **Tools:** one-tap fly, no cost, god mode, ghost, tame nearby, kill nearby, remove drops and dev commands, plus heal and repair and the free-build toggle. A spawn row takes an item or creature name and an amount and spawns it.
- **Commands:** every KingsTweaks command with an on/off switch for whether it appears in `/kt`. A command the server has disabled outright is shown as disabled rather than offered.
- **Permissions:** every admin, and what each one is allowed to do. Pick an admin to switch their individual rights on and off.

## Permissions

*Off by default, and off means exactly what the mod did before: every admin can do everything. Nobody loses anything by updating.*

- **Superadmins** are the people who own the server, listed by Steam64 ID in the config. A superadmin has every right, and is the only one who can change what other admins may do. Whoever is running a listen server is always a superadmin.
- **Admins** can be given rights one at a time: kicking, banning, the allowed list, making admins, changing rights, server settings, the admin tools, showing and hiding commands, teleporting, warps, purging bodies and spectating.
- Turn on `PermissionsEnabled` and admins are held to what they have been given. Leave it off and nothing changes.
- Every right is checked **on the server**, from the server's own records, on every single action — the in-game menu only decides which buttons are worth drawing. A client that lies about its own rights gets refused anyway, and the refusal says which right was missing.
- `SuperAdmins` and `PermissionsEnabled` can only be changed by a superadmin, so an admin can't promote themselves. Rights are kept in `dev.craz.kingstweaks.permissions.txt` beside the config.

## Spectating

- `/spectate <name>` puts the camera behind that player and follows them; `/spectate` again stops and puts you back where you were. Move the mouse to swing the view around them.
- Your own character comes along, because the game only loads the world around a player. It's put into god and ghost mode so nothing attacks it and it can't die while nobody is driving, and your view of it is hidden so it isn't in the shot. Other players can still see it standing there — Valheim has no way to hide a character from another player.
- Needs the spectate right, and the target has to be loaded; teleport to them first if they're across the map.

## Character size

- `/size 1.5` makes your character half again as tall; `/size 1` puts you back to normal; `/size` on its own tells you where you are.
- The number lives on your character, so everyone sees everyone else at the size they chose rather than each player seeing a world of ordinary-sized people.
- The server sets the range — 0.5 to 1.5 by default — and can restrict it to admins or turn it off. Worth remembering that a bigger character has a bigger hitbox and longer reach, which matters on a PVP server.

## The white deer

*Off by default.*

- Valheim already has a white deer — the prefab is `Deer_White` — but it isn't in any spawn list, so nobody ever sees one. This puts it into the world.
- It appears in the same places ordinary deer live, with the same weather and time-of-day conditions, because its spawn entry is copied from the ordinary deer's. Only the chance and the interval are changed: 1% every half hour by default, which is genuinely rare.
- It has 30 health and drops two Deer Meat plus a **Trophy Deer White**, guaranteed — unlike the ordinary deer trophy, which is a coin flip. Those drops are the creature's own, so nothing here changes them.
- Nothing is built or modified, so it's the game's own creature with the game's own behaviour, and every client already has it. `/ktcheck` reports whether it was found and how many spawn lists it went into.

## Crafting

- **Search the crafting list:** a Search button on the crafting panel narrows the recipes to what you type. `/find bronze` does the same from chat, and `/find` on its own clears it. It filters the list the menu is built from rather than rearranging the window, so nothing about the crafting UI changes.

## Server tools

- **Server password saver:** the password you enter when joining a server is saved and entered automatically next time. If it changes, you're prompted for the new one.
- **Continue button** on the main menu, loading whatever you played last: the same character plus either that world or that server.
- **World backups:** after the game saves, the world files are copied into a backups folder, keeping as many as you choose and deleting the oldest.
- **Scheduled restarts:** at times you set, everyone is warned in chat, the world is saved and the server closes. Starting it again is up to your start script or service, since a game can't relaunch itself.
- **Playtime tracking** per player, surviving restarts, readable with `/playtime`.
- **Version enforcement:** players must run the same KingsTweaks version to join, matched exactly, and anyone without the mod is disconnected. On by default — update the server and your players together, or turn it off while you're mid-update.

---

## Installation

Requires BepInEx.

1. Install `KingsTweaks.dll` in `BepInEx/plugins` on the server and on each client.
2. Launch the game once. The config file is created at `BepInEx/config/dev.craz.kingstweaks.cfg`.
3. Nothing needs configuring to start with. Every feature has a sensible default, and `ModEnabled` under `01 - General` is the master switch: turn it off and the whole mod stands down without being uninstalled.

If something that used to work stops, run `/ktcheck` before anything else. It names every part of the game the mod reaches for and says which ones it found, so a feature broken by a game update shows up as one line instead of a mystery.

Updating is safe: if a release moves settings into different sections, your existing values are carried across to the new layout automatically. Your own display preferences live in a separate file, so a server never overwrites them.

Alongside the config, the mod keeps its own plain-text files in `BepInEx/config`, all named `dev.craz.kingstweaks.*`:

| File | Holds | Back it up |
|---|---|---|
| `characters.txt` | server-side characters: inventories and skills | **yes** — this is player data |
| `permissions.txt` | what each admin is allowed to do | yes |
| `banreasons.txt` | why each banned player was banned | yes |
| `warps.txt` | the warps `/addtp` created | yes |
| `teams.txt` | teams and their members | yes |
| `homes.txt` | each player's `/sethome` | yes |
| `playtime.txt` | time on the server per player | yes |
| `passwords.txt` | server passwords you've joined with | no — it's yours, not the server's |
| `lastsession.txt`, `hintshown.txt` | what the Continue button loads; whether you've seen the first-run hint | no |

The world backups feature copies the world files, not these — they live with the config, so make sure whatever you back up covers both.
