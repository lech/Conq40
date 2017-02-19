# Conq 40

This is a brutal Insurgency configuration for the Conquer game mode. This config always starts the game with 40 bots at the highest difficulty setting and always attempts to keep a high count running around on the server. Human player counts do not influence the number of bots that spawn.

## Requirements

A decent enough server for hosting 8 players and 40 bots.

## Current features
- There are no points awarded for failure.
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

## Works in progress
- Bots armed with RPGs should be firing at closer ranges on single players instead of only at groups. I'm still trying to figure these settings out and fine-tune them for potential point-blank action.

## Installation

- Backup your current configuration, vanilla or otherwise.
- CHANGE THE DEFAULT RCON PASSWORD!
- Copy and paste the files into their appropriate directories.

## Known issues

- If you're running on a shared host, you may notice stutter and this might not run so well. If that happens you may want to scale back the number of bots or opt for a better host.
