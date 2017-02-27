# Conq 40

This is a very punishing, _ultra-brutal_ configuration for the Insurgency Conquer game mode. This config always starts the game with 40 bots at the highest difficulty setting and always attempts to keep a high count running around on the server. Human player counts do not influence the number of bots that spawn.

## Current settings and features

__Server__

- The `server.cfg` should serve as a _working example_ only, you should be able to incorporate most of these settings into your existing configs with minimal effort.
- Voting is limited to map changes, kicking and muting players only.
- The dead can talk and type to the living, this serves to help the living die faster.
- Currently the map cycle is set for daylight maps only. If you can win a map with pistols only on night mode without cheating, I salute you.

__Human players__

- Human players start with only 15 supply points.
- There are no points awarded for round failure.
- Human players are soft, weak and tire easily. This is merely an observation and not a feature.

__Bots__

- 40 bots set to brutal at start.
- Because 40 is the theme, bots start with 40 supply points.
- Bots do full damage, so don't stand behind paper thin walls.
- RPG equipped bots will fire on single players at shorter ranges.
- Destroying all caches doesn't eliminate the bot population as in normal games. Instead, it only reduces their numbers and angers them.

__Environment and Gameplay__

- Explosive damage models have been modified to make explosions far more deadly, you are now truly subject to your own stupidity.
- The RPG, grenade and cache explosion radius is larger - Dump and run or prepare to take a flying dirt nap.
- Caches take 4x more damage to destroy - 800 points versus the default of 200.
- The time it takes to capture an objective is double - 1.5 Minutes vs 45 seconds making holdouts stressful.

## Requirements

A good host that can handle running 8 players and 40 bots. In testing, a 10 Players Insurgency Standalone host from gameservers.com can run this configuration acceptably.

## Installation

- MAKE A BACKUP of your current configuration. Vanilla or otherwise.
- DON'T BE STUPID. CHANGE THE DEFAULT RCON PASSWORD!
- Edit the files and place them into their appropriate directories on your server.

## CVARS
See http://ins.jballou.com/cvarlist.php if you have doubts or questions for any of the config settings. Or produce your own:

1. Add `-condebug` to your Insurgency launch options and run the game.
2. In the console type the following to get a list:
 - `cvarlist`
 - `cvarlist mp`
 - `cvarlist sv`
3. find a `console.log` in your game directory after exiting the game.

## Known issues

- You may notice gameplay stutter or the game not running so well on your server under this configuration. Scaling back the number of bots does improve most performance issues while while maintinaing the difficulty. Stuttering is more apparent on open maps like Burhiz when many players, bots and bullet projectiles are produced in a tight area.

- On map change, loading the next map may throw a `Host_Error: CL_ReadPreserveEnt: u.m_nNewEntity == MAX_EDICTS || u.m_nNewEntity < 0` error on the client if the server is a locally hosted Windows dedicated SRCDS. Reconnecting to the server works and *nix servers appear unaffected at this time.

- Combing through the logs, the server produces streams of `Weapon spawning in solid!` and `Performance Warning choosing best spawn` warnings.
  - I suspect the `Weapon spawning in solid!` warning may be weapons dropping from dead players and enemies.
  - The `Performance Warning choosing best spawn` warning occurs when a large number of bots is spawned in at once at the same spawn point. Lowering wave timers and increasing the `mp_conquer_auto_reinforce_at_bot_count` number reduces these warnings after a round start.
