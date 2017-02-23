# Conq 40

This is a brutal Insurgency configuration for the Conquer game mode. This config always starts the game with 40 bots at the highest difficulty setting and always attempts to keep a high count running around on the server. Human player counts do not influence the number of bots that spawn.

## Requirements

A decent enough server for hosting 8 players and 40 bots.

## Current features
- There are no points awarded for failure.
- Bots do 2 damage instead of 0.6.
- Human players start with 13 supply points.
- Bots start with 28 supply points.
- Voting is limited to kicking players and map changes only.
- Caches should take twice as much to destroy.
- Grenade and cache explosion radius is a bit larger. Run.
- Explosive damage models have been doubled, you are now truly subject to your own stupidity.
- The time it takes to capture an objective is doubled. 1.5 Minutes vs 45 seconds.
- Destroying all caches doesn't reduce the bot population to zero, it only reduces them by 25%.
- Follow up wave timers have been cut in half.
- Killed all but 2 bots? REINFORCEMENTS ARE ON THEIR WAY!
- Bots respond to objectives from further away, expect resistance.

## Work in progress
- I want bots with a RPG to fire upon single players at close range instead of just at groups at medium/long ranges. I'm still trying to fine-tune these settings for a closer, potentially point-blank RPG responses. Why? Because surprise, you blew up!

## Installation

- MAKE A BACKUP of your current configuration. Vanilla or otherwise.
- DON'T BE STUPID. CHANGE THE DEFAULT RCON PASSWORD!
- Copy, paste and edit the files you need into their appropriate directories.
- See http://ins.jballou.com/cvarlist.php if you have doubts for any of the config settings.

## Bugs and known issues

- If you're running on a shared host, you may notice stutter and this might not run so well. If that happens you may want to scale back the number of bots or opt for a better host. Preferably the latter.
- On map change, loading the next map may throw a ``Host_Error: CL_ReadPreserveEnt: u.m_nNewEntity == MAX_EDICTS || u.m_nNewEntity < 0`` error on the client if the server hosted on Windows dedicated server (not fully tested under *nix yet). Not quite sure what's causing this, but reconnecting to the server works.
