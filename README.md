# Conq 40

This is a very punishing, _ultra-brutal_ configuration for the Insurgency Conquer game mode. This config always starts the game with 40 bots at the highest difficulty setting and always attempts to keep a high count running around on the server. Human player counts do not influence the number of bots that spawn.

## Requirements

A good host that can handle running 8 players and 40 bots. In testing, a 10 Players Insurgency Standalone host from gameservers.com can run this configuration acceptably.

## Current settings and features

__Server__

- Voting is limited to kicking players and map changes only.

__Human players__

- Human players start with 15 supply points.
- There are no points awarded for failure.
- Human players are soft, weak and tire easily. This is merely an observation and not a feature.

__Bots__

- 40 bots.
- Bots start with 28 supply points.
- Bots do double the damage, don't stand behind paper walls.
- Bots respond to objectives from further away, expect resistance.
- Increased response ranges. Reinforcements are always moving your way when you so much as think about taking an objective.
- Destroying all caches doesn't reduce the bot population to zero, it only reduces them by 25%. 30 versus 40 bots, only slightly easier.

__Environment and Gameplay__

- Explosive damage models have been doubled, you are now truly subject to your own stupidity.
- Grenade and cache explosion radius is a bit larger - Dump and run or take a dirt nap.
- Caches take 4x more damage to destroy - 800 points versus the default of 200.
- The time it takes to capture an objective is double - 1.5 Minutes vs 45 seconds.
- Follow up wave timers have been cut in half.

## Works in progress
- I want bots with a RPG to fire upon single players at close range instead of just at groups at medium/long ranges. I'm still trying to fine-tune these settings for a closer, potentially point-blank RPG responses. Why? Because surprise, you blew up!

## Installation

- MAKE A BACKUP of your current configuration. Vanilla or otherwise.
- DON'T BE STUPID. CHANGE THE DEFAULT RCON PASSWORD!
- Copy, paste and edit the files you need into their appropriate directories.


## CVARS
See http://ins.jballou.com/cvarlist.php if you have doubts for any of the config settings. Or make your own:

1. add -condebug to your launch options
2. Run the game and run the following to get a full list:
 - `cvarlist`
 - `cvarlist mp`
 - `cvarlist sv`
3. find a `console.log` in your game directory after exiting the game.

## Bugs and known issues

- If you're running on a shared host, you may notice stutter and this might not run so well. If that happens you may want to scale back the number of bots or opt for a better host. Preferably the latter.
- On map change, loading the next map may throw a `Host_Error: CL_ReadPreserveEnt: u.m_nNewEntity == MAX_EDICTS || u.m_nNewEntity < 0` error on the client if the server hosted on Windows dedicated server when hosted locally. Not quite sure what's causing this, but reconnecting to the server still works. All *nix hosted servers appear unaffected at this time.
- Currently the server may throw a lot of `Weapon spawning in solid!` and `Performance Warning choosing best spawn` errors into the logs.
