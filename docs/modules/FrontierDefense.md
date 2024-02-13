---
tags:
  - "#titanfall"
  - squirrel
  - cursed-titanfall
  - scripts
  - modding
---
# Frontier Defense
-------------------------
## Features
---------------
- Adds bosses from the campaign as entities capable of being spawned in multiplayer
- Boss spawn titan spawns in some Frontier Defense maps
	- Complex
	- Forward Base Kodai
	- Homestead
	- Eden
	- Boomtown
	- Black Water Canal
	- Wargames
- Modified wave layouts and/or harvester locations on some maps
	- Complex
## Bosses
- ### Spawn Functions
	- Create npc titan entity and register using the FD elite functions found in Zanieon's fork of NorthstarMods fd-experimental branch
	- Spawn functions additionally check if a boss theme is playing and add to the playing tracks while using `EmitSoundOnEntity` for all players to play the selected track
	- Ash intro function and music handling in `scripts/vscripts/sp/sp_boomtown_end.nut#727`