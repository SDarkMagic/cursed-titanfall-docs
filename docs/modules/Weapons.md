---
tags:
  - "#titanfall"
  - squirrel
  - cursed-titanfall
  - scripts
  - modding
---
# Weapons
--------------
Responsible for the individual weapon code changes and registering them as callbacks via the methods defined in [[Framework#Weapon Callbacks|Weapon Callbacks]]
If a weapon does not have a unique script in the vanilla game, the script for it will be added here rather than creating a new one in [[Framework]]

# Features
--------------
### Devotion
- Increased magazine size
- Increased maximum fire rate
- Now does significantly more damage against titans as well
- No longer requires critical hits/weak point damage to hurt titans
### R-201
- Gives the user flightcore salvo rockets while rodeoing a friendly titan. Primary usage is to be an anti-titan turret while chilling on a friend :)
### Alternator
- Reloading causes the user to phase shift for a portion of the reload based on the percent of the magazine consumed before reloading.
### Car SMG
- Applies knockback when hitting an entity. This effect is more noticeable on larger enemies, such as titans
### R-97
- Causes enemies killed by it to explode with the explosion dealing damage equal to 3 times the killed enemies health. This means that killing enemies with more health with it will produce higher damage explosions with the same general blast radius.
### Volt
- Deals damage when attacking titans regardless of critical hits
- After dealing 2500+ damage, reloading grants a battery
### Softball
- Increased grenade explosion radius
- Increased grenade explosion damage
- Increased grenade explosion knockback
- Slightly decreased fire rate
- Slightly decreased reload speed
- Grenades now create an electric smoke field on impact
### SMR
- Missiles now create a small cluster explosion at the point of impact
- Slight explosion damage decrease
- Slightly increased explosion radius
### EPG
- Changed projectile model
- Projectile now creates a prowler owned by the player on impact
### Double Take
- Converted to fully automatic
- Modified damage. Two body shots should now kill a pilot at full health
- Lowered fire rate slightly
### DMR
- Deals increased damage
- Capable of damaging titans regardless of whether it's a crit hit
- On client uses ion laser effect and sounds for firing
- Hitscan
### Spitfire
- Creates a thermite burn source on impact
- Canonically accurate to the name now
### B3 Wingman
- Teleports the player to the shot target. This includes out of bounds you have been warned
	- *Note*: The teleport function will move you to a point slightly behind where you hit with the shot. This means if you accidentally clip through a wall, you can a nearby surface opposite the direction you would like to be moved and potentially move back in bounds
### Kraber
- Fires explosive rounds similar to Tone's splasher round aegis upgrade
- 50% chance for every magazine to contain a bullet that can misfire. The chance of the misfire increases the more shots you make.
- Significantly increased critical damage to titans
### P2016
- No longer does damage when hitting an enemy
- Has a random chance of killing the user and publicly shaming them when hitting an enemy
- When hitting an enemy, there is a 1/~48 chance to kill every enemy on the enemy team.
	- *Warning*: Due to how the functions used internally to get the enemies work, if an entity is being spawned when this kill all event occurs, it may cause a server crash
### Arc Grenade
- No longer damages spectres or reapers
- Hacks hit reapers
- Will attempt to hack any spectres hit by its explosion
	- *Note*: The hitbox for this is not always consistent, and if the spectres get knocked down by the blast, they most likely will not be hacked
### Charge Rifle
- Trigger must be held down after firing for it to actually deal damage
- Pushes the user backwards when fired
### Thunderbolt
- Drags enemies along with the projectile now
- Equipping the Pro Screen mod causes the user to also be pulled along with the projectile