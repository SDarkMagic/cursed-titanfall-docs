---
tags:
  - squirrel
  - modding
  - titanfall
  - cursed-titanfall
---
# Cursed Titanfall
## Modules
This mod is divided into different sub modules to allow for easier control of the features it provides.
- [[Core|Core]]
- [[Framework|Framework]]
- [[Weapons|Weapons]]
- [[FrontierDefense|Frontier Defense]]
- [[Titans|Titans]]

## Features
*Individual feature listings can be found along side the corresponding module documentation*

*Additionally, a list of planned feature ideas and ones that may not yet be in the documentation can be found in the [[#Todo]] section*

Have a feature idea you don't see in the [[#Todo]] or individual [[#Modules|Module]] features? Suggest a new feature or idea to add to the mod through [this google form](https://forms.gle/2BXSoWrouU7uV8Hw6)
## Known Bugs
- [x] Spitfire projectiles causing error when caught by ion vortex shield
- [ ] Killing enemy pilots while they are lobotomizing a titan crashes the server
- [x] wingman elite failing to handle on fire properly
- [ ] Colony crashes wave 5 at ~74 enemies remaining
- [ ] Blisk is still rodeoable?
- [ ] boss titans not spawning when more than one is present in the waves
- [x] Wingman elite still using modified kraber OnPrimaryAttack function
- [x] Viper insta-dying on kodai
- [ ] Devotion missing reload activity on server causing a crash
- [x] Devotion firerate is too high; Causes server side warning, and must be under .2f
- [ ] Player dies to spitfire failure to get load screen tip
- [x] grunts might have guaranteed p2016 team wipe
- [x] Elite northstar trying to execute player
- [x] Boss titan reset health loop attempting to set health even if the entity is dead
- [ ] Server boot error:
 ```
[05:12:29] [NORTHSTAR] [info] Running custom SERVER script callback "S2S_DropshipInit"
[05:12:30] [NORTHSTAR] [info] Running custom SERVER script callback "NorthstarCustomPrecache"
[05:12:30] [NORTHSTAR] [info] [DEDICATED SERVER] Error: [1]
[05:12:30] [NORTHSTAR] [info] [DEDICATED SERVER] KeyValues Error: RecursiveLoadFromBuffer:  got EOF instead of keyname in file scripts/weapons/mp_weapon_peacekraber.txt
WeaponData, (*RUI_CrosshairData*), (*Crosshair_2*),

[05:12:30] [NORTHSTAR] [info] [DEDICATED SERVER] Error: [2]
[05:12:30] [NORTHSTAR] [info] [DEDICATED SERVER] KeyValues Error: RecursiveLoadFromBuffer:  got } in key in file scripts/weapons/mp_titanweapon_arc_cannon.txt
WeaponData, RUI_CrosshairData, Crosshair_1, Element0,

[05:12:30] [NORTHSTAR] [info] Running custom SERVER script callback "DropPodSpawn_Init"
```
- [x] Spitfire broke again - Ion vortex shield refire issue when attempting to attach projectile to enemies
- [x] Tether traps instantly dooming nuke titans?
- [ ] boss titans still rodeoable sometimes
- [ ] ```[05:05:06] [SCRIPT SV] [info] SCRIPT ERROR: [SERVER] Die: passing in projectile as attacker
[05:05:06] [SCRIPT SV] [info]  -> target.Die()
[05:05:06] [SCRIPT SV] [info]
CALLSTACK
*FUNCTION [KillTargetThenExplode()] _weapon_callbacks.nut line [360]
*FUNCTION [DetonateOnDeath()] _weapon_callbacks.nut line [352]
*FUNCTION [CodeCallback_DamageEntity()] _codecallbacks_common.gnut line [115]


abnormal program termination
0024:fixme:msvcrt:__clean_type_info_names_internal (0000000005168788) stub
nswrap: northstar exited with status 3
nswrap: killing xvfb
nswrap: waiting for children to exit```
- [ ] Enemy spawned prowlers cause crash on wave reset
- [x] Disembarking while hover is active with viper thrusters by moving to a higher location so it registers as standing. Should just need an `IsValid` check on the weapon
- [ ] Kraber bullets crash when in vortex shield
- [x] ![[Pasted image 20240927182905.png]]
- [ ] *FUNCTION [RemoveMod()] weapons/mp_titanability_hover.nut line [74]
*FUNCTION [unknown()] weapons/mp_titanability_hover.nut line [141] - entity is null
- [x] Arc Titans causing crashes after giving ronin passive (have not been able to replicate since)
      ```
    [02:29:14] [SCRIPT SV] [info] SCRIPT ERROR: [SERVER] Entity is null
	[02:29:14] [SCRIPT SV] [info]  -> titan.EndSignal( "OnDeath" )
	[02:29:14] [SCRIPT SV] [info] ai/_ai_emp_titans.gnut line[25]
## Todo
- [ ] Boost to summon a reaper. Reaper kills count for player.
- [ ] Burst fire on predator cannon close range power shot fire
- [ ] Replace laser tripwire with a temporary arc field that drains enemy shields and converts it them to energy for ion (Probably an aegis upgrade since shields are more common in FD)
- [ ] Celebratory effect when spawning weapon from frag
- [x] Nuke Eject has a gravitational field around it when activated (only on ogre chassis)
- [x] Increase Kraber Crit damage
- [x] Increase crit damage for northstar when using the threat optics kit
- [x] Enhanced Payload flightcore clusters do less damage and last for a shorter duration
- [x] Ronin melee parry costs 10% core charge per rounded cell of HP the enemy has to auto execute
- [x] Override elite nuke eject code on boss titans
- [x] Add guardian blocks on p2016 for NPC fire events to check if hit entity is a player
- [x] smg grants batt on reload if damage threshold is met
- [x] Give Kraber Northstar Railgun damage output, remove chance of misfire on first shot
- [ ] Charge time on double take, fires two bolts on release in quick succession for big damage
- [x] Having enhanced payload kit on northstar causes flightcore to shoot cluster missiles
- [ ] Trace Rifle L-Star
- [ ] Manually reloading the alternator will cause the player to phase for the duration of the reload animation. Refund ammo to the magazine on critical hits for more control of when this phase occurs.
- [ ] Markiplier intro after the "Who's Mark" line plays
- [ ] Fix issue where player spawned prowlers are damageable by the owner
- [ ] Add gacha pull animation to the p2016 on hit
- [x] EnableDoomed on enemies if titan when triggering team wipe. Also use Die instead of TakeDamage to circumvent damage scaling by mode
- [ ] Vortex shield at close range absorbs enemy titan shields
- [ ] Re-implement devotion overheat mechanic
- [ ] Add effects and sound for ronin parry activation and duration of parry window
- [ ] Figure out if it's possible to show sword melee animation and model on all titan classes exclusively server side (probably not)
- [ ] Limit amount of particle effects that can be caused simultaneously by weapons like the smr and spitfire to reduce client lag
- [ ] Increase parry window time to compensate for player lag
- [x] Allow dashing while using laser core
- [x] Particle accelerator primary fire drains energy instead of using ammo. Hitting targets regenerates energy. Using the ADS shots uses more energy.
- [x] Northstar gets cloaking ability
- [ ] Re-45 applies stim effect while drawn
- [ ] Landing hits with the Re-45 will return a round to the magazine. Kills with this weapon will grant a stacking damage bonus until it is reloaded
- [ ] Smart core predator cannon grunts
- [ ] Random chance of spawning on the enemy team when joining in frontier defense
- [x] Make reaper warpfall on core 3 upgrade a random chance event
- [x] Remove friendly collision on prowlers
- [x] Retime boss titan on kodai
- [x] Lower pilot r201 damage
- [x] Ion absorbs energy/electric damage and recharges either shields or energy meter from them - use in tandem with shield idea
- [x] Give tone passive sonar in a radius around her (Tied to primary weapon fire)
- [ ] give thunderbolt `DF_RAGDOLL`
- [ ] Cold war shoots batteries sometimes
- [x] Remove 3-round capacity limit for burst fire kit on tone
- [x] Replace an AR with flightcore rockets
- [ ] Maintain R201 loadout when swapping back from rodeo-ing
- [ ] A-wall applies flat damage multiplier rather than adding amped flag
- [ ] Add monarch heal rounds to heal score callback
- [ ] Add client side RUI for energy transfer health pool
- [x] Phoenix kit for scorch
- [ ] Nuke Core titan
	- [ ] Core ability is equivalent to a nuke eject explosion, however the titan does not get destroyed
	- [ ] thermal shield for tactical?
	- [ ] Stryder chassis
	- [ ] electric smoke as utility ability in addition to anti rodeo smoke.
	- [ ] deployable that uses the tether trap model and functions as a proximity mine
	- [ ] Cloak ability for tactical
	- [ ] Primary is a close range explosion? Potentially just punching but add an explosion on impact?
- [ ] Warp core titan
- [ ] Allow lockons to boss titans (probably a client side change)
- [x] Allow nuke eject to trigger before doomed state
- [ ] Smr missiles delayed immediately after firing. Stall in air then rapidly accelerate to deal more damage.
- [x] Allow archer to lock onto players (This may need to be a client side change unfortunately) | Done by MasterLiberty and has been added to the mod with permission
- [ ] Smart pistol misses every shot while locked on
- [ ] Tighten eva8 spread. Shift fire offset to br akward. More ideal have the reticle be passed through a perspective transform to align with whatever plane the player is currently targetting. Projectiles shoot at an angle rather than just starting from an offset.
- [x] Disable collision on friendly reapers
- [x] Remove hacked reapers from spawned npc array? (Done by FD on leeched callback)
- [ ] change minimap icon color for friendly reapers
- [ ] A-wall no longer a deployable. Attach to player position and offset forward. Remain active for a set duration shrink size partially (Zanieon has already figured this out, either ask for details or wait until it gets added to fork)
- [ ] Add the 30-30 with shattercaps. 3 body shots to a pilot to kill, headshots are oneshot (while adsed) if client side version of the mod is installed, use the actual 30-30 model. Otherwise use g2 model
- [ ] Satchel becomes a proximity mine
- [ ] Mozambique projectiles grow with travel time
- [ ] Add guardian blocks after weapon callback loops
- [ ] Throw hands (I will not elaborate further on this)
- [ ] Ion gets shield mechanic similar to Asuka R# but uses energy instead of mana
- [ ] Legion shoots thermite for bullets
- [ ] Reapers can spawn ticks in attrition
- [ ] Northstar plasma railgun at max charge. Passively charges strength after firing. Shorter wait time causes less powerful shot
- [ ] L-star is a Charge rifle-esque weapon. On click force locks user into charging the weapon. On fire fires an ion laser core for a short duration
- [ ] Hemlok shoots multiple bursts simultaneously (equivalent to one mag?) maybe give shotgun spread
- [ ] Add boss titans to more FD maps
- [ ] Graviton lance
	- [ ] Model import
	- [ ] Tracer effects
	- [ ] muzzle flash effects
	- [ ] Grenade model/effects?
	- [ ] General functionality
		- [x] Current issue seems to be with the seekers spawning within one another, immediately triggering their damage callback
- [x] Reaper global stack
- [x] Ronin gets to parry
- [x] Add 25 tick limit
- [x] Ronin with Thunderstorm passive is now an arc titan
- [x] Lower probability of p2016 insta teamkilling. Add logic to fired projectile instead of the gun.
- [x] DMR shoots ion laser
- [x] Allow thunderbolt projectile to drag player if they have pro screen equipped
- [x] Energy syphon causes monarch's shots to take hp from hit enemies and fill a meter. Shooting teammates will deplete this meter and refill their HP a respective amount
- [x] Arc grenade auto-hacks spectres
- [x] Spitfire shoots some kind of firestars
- [x] Add dodge message announcement when upgrade 3 is triggered
- [x] CAR smg applies knockback to entities hit by shots if they are movable
- [x] Make Viper thrusters default flight speed for northstar hover and flightcore. Change viper thrusters to convert hover into a toggle ability with cooldown based on a multiplier of how long you were airborn for. Additionally allow dodging while airborn with viper thrusters
- [x] arc grenade hacks reapers. Look at leech_spectres function for implementation inspiration
- [x] Give thunderbolt projectiles a gravitational field similar to grav stars (currently just have arc titan emp field applied to them will need to remove)
- [x] Legion shields absorb shots to refill mag. May need to be based on damage absorbed rather than individual shot count esp because of scorch thermite projectiles
- [X] Wingman converted to hitscan. Instant teleport the player to the targetted location if in bounds.
- [X] Scorch immune to own fire by default. Mod adds healing or shield regen when in own fire
- [X] Epg shoots ragdolled prowlers that become active once they collide with something. Lower damage on hit player to prevent one shots. Prowler kills count for players kills. Limit max amount of prowlers at a time through use of a global stack.
- [X] Ion tripwwire lasts longer
- [X] Double take becomes full auto at leadwall firerate. Two shots to kill on body. Headshots still innstakill. Add hipfire reticle.
- [X] Shooting the spitfire will kill the player if they do not move far enough after shooting it. Prevents camping.
- [X] Infinite (20) ricochet on kraber
- [X] Softball has increased blast radius; spawns electric smoke on detonation
- [x] Increase flight ceiling for northstar
- [X] Lower kraber misfire probability slightly. Add explosion effect when misfire occurs
- [X] Devotion has deeper mag. Fire rate starts slower but increases to significantly faster. Explode if the mag empties while at max fire rate.