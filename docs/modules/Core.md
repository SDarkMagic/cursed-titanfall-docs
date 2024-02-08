---
tags:
  - "#titanfall"
  - squirrel
  - cursed-titanfall
  - scripts
  - modding
---
# Core
---------
Commonly utilized functions and structs that may be required by any of the other modules in the mod.

# `sh_datatypes.nut`
This file contains any new custom datatype structs that may be needed across multiple modules. 
- `ProjectileCollisionParams`
	- `projectile` - entity; The entity object that represents the projectile.
	- `pos` - vector; The projectile's position represented by a 3 point vector
	- `normal` - vector; The normal surface to the projectile's movement
	- `hitEnt` - entity; An entity object representing the entity that is being hit by the projectile
	- `hitbox` - int;
	- `isCritical` - bool; True if the hit should apply the critical damage modifier

# `team_entity_handler.nut`
Helper functions for managing global stacks that handle various child entities that may be spawned by other parts of the mod