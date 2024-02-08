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
*Additionally, a list of planned features and ones that may not yet be in the documentation can be found in the [[#Todo]] section*

```dataviewjs
dv.list()
```
```dataviewjs
dv.current()
```
```dataviewjs
dv
```
## Known Bugs
- [x] Spitfire projectiles causing error when caught by ion vortex shield
      ```
    [20:01:33] [SCRIPT SV] [info] SCRIPT ERROR: [SERVER] Empty table name.
	[20:01:33] [SCRIPT SV] [info]  -> local fxTableHandle = GetImpactEffectTable( impactData.impact_effect_table )
	[20:01:33] [SCRIPT SV] [info]
	CALLSTACK
	*FUNCTION [Vortex_SetImpactEffectTable_OnProjectile()] weapons/_vortex.nut line [1281]
	*FUNCTION [Vortex_ProjectileCommonSetup()] weapons/_vortex.nut line [1262]
	*FUNCTION [Vortex_FireBackProjectileBullet()] weapons/_vortex.nut line [1148]
	*FUNCTION [DoVortexAttackForImpactData()] weapons/_vortex.nut line [1247]
	*FUNCTION [VortexPrimaryAttack()] weapons/_vortex.nut line [1042]
	*FUNCTION [OnWeaponNpcPrimaryAttack_titanweapon_vortex_shield()] weapons/mp_titanweapon_vortex_shield.nut line [316]
      ```
- [ ] wingman elite failing to handle on fire properly
- [ ] Wingman elite still using modified kraber OnPrimaryAttack function
- [ ] Viper insta-dying on kodai
- [ ] Devotion missing reload activity on server causing a crash
- [x] Devotion firerate is too high; Causes server side warning, and must be under .2f
- [ ] Player dies to spitfire failure to get load screen tip
```
[14:52:32] [NATIVE SV] [info]
[14:52:32] [SCRIPT SV] [info] Warning: AI Path failsafe at <-916.247, 884.993, 569.409>
[14:52:33] [SCRIPT SV] [info] SCRIPT ERROR: [SERVER] getrandom(): Array is empty
[14:52:33] [SCRIPT SV] [info]  -> return potentialIds.getrandom()
[14:52:33] [SCRIPT SV] [info]
CALLSTACK
*FUNCTION [GetHintIDFromHintGroups_WeightedByPreviousViews()] sh_death_hints.gnut line [820]
*FUNCTION [GetBestDeathHintForNPCTitle()] sh_death_hints.gnut line [233]
*FUNCTION [OnPlayerKilled()] mp/_gamestate_mp.nut line [630]
*FUNCTION [PlayerOrNPCKilled()] mp/_base_gametype.gnut line [745]
*FUNCTION [CodeCallback_OnPlayerKilled()] mp/_base_gametype_mp.gnut line [249]
*FUNCTION [SpinOff()] NATIVE line [-1]
*FUNCTION [SpitfireBulletHit()] _spitfire_projectile_callback.nut line [44]
*FUNCTION [OnProjectileCollision_weapon_lmg()] weapons/mp_weapon_lmg.nut line [125]
```
- [x] Elite northstar trying to execute player
```[06:48:57] [SCRIPT SV] [info] Player entity (148: npc_titan sniper_titan [148]) attempting to melee entity (3: player Dellfox6800 [3]) TitanVsTitanMelee
[06:48:57] [SCRIPT SV] [info] SCRIPT ERROR: [SERVER] Entity class "CNPC_Titan" doesn't match required class for this index or function call
[06:48:57] [SCRIPT SV] [info]  -> attacker.Lunge_ClearTarget()
[06:48:57] [SCRIPT SV] [info]
CALLSTACK
*FUNCTION [MeleeThread_TitanVsTitan_Internal()] melee/_melee_synced_titan.gnut line [218]
*FUNCTION [MeleeThread_TitanVsTitan()] melee/_melee_synced_titan.gnut line [134]
*FUNCTION [PlayerTriesSyncedMelee()] melee/sh_melee.gnut line [597]

[06:48:57] [SCRIPT SV] [info] LOCALS
[bossPlayer] NULL
[burnCardTarget] ENTITY (player Dellfox6800 [3] (player "Dellfox6800" at <-9059.52 -4209.49 580.401>))
[titanSubClass] "stryder"
[dataStruct] unknown struct
[func] CLOSURE
[target] ENTITY (player Dellfox6800 [3] (player "Dellfox6800" at <-9059.52 -4209.49 580.401>))
[attacker] ENTITY (npc_titan sniper_titan [148] (NPC "npc_titan_stryder_sniper_boss_fd_elite" at <-9213.4 -4101.18 580.391>))
[action] unknown struct
[this] TABLE
[target] ENTITY (player Dellfox6800 [3] (player "Dellfox6800" at <-9059.52 -4209.49 580.401>))
[attacker] ENTITY (npc_titan sniper_titan [148] (NPC "npc_titan_stryder_sniper_boss_fd_elite" at <-9213.4 -4101.18 580.391>))
[action] unknown struct
[this] TABLE
[target] ENTITY (player Dellfox6800 [3] (player "Dellfox6800" at <-9059.52 -4209.49 580.401>))
[player] ENTITY (npc_titan sniper_titan [148] (NPC "npc_titan_stryder_sniper_boss_fd_elite" at <-9213.4 -4101.18 580.391>))
[this] TABLE
```
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
```
[01:23:08] [SCRIPT SV] [info] SCRIPT ERROR: [SERVER] Entity class "CCrossbowBolt" doesn't match required class for this index or function call
[01:23:08] [SCRIPT SV] [info]  -> projectile.SetDoesExplode( false )
[01:23:08] [SCRIPT SV] [info]
CALLSTACK
*FUNCTION [SpitfireBulletHit()] _spitfire_projectile_callback.nut line [36]
*FUNCTION [OnProjectileCollision_weapon_lmg()] weapons/mp_weapon_lmg.nut line [125]

[01:23:08] [SCRIPT SV] [info] LOCALS
[result] true
[collisionParams] TABLE
[player] ENTITY (npc_titan npc_titan_atlas_stickybomb [382] (NPC "npc_titan_atlas_stickybomb" at <2858.09 1094.73 -127.969>))
[isCritical] false
[hitbox] 0
[hitEnt] ENTITY (worldspawn [0] at <0 0 0>)
[normal] <-0.707107, -0.707107, 0>
[pos] <2967.33, 2120.63, 94.6843>
[projectile] ENTITY (crossbow_bolt [895] at <2967.33 2120.63 94.6843>)
[hitParams] unknown struct
[this] TABLE
[@ITERATOR@] 1
[callback] CLOSURE
[@INDEX@] 0
[params] unknown struct
[isCritical] false
[hitbox] 0
[hitEnt] ENTITY (worldspawn [0] at <0 0 0>)
[normal] <-0.707107, -0.707107, 0>
[pos] <2967.33, 2120.63, 94.6843>
[projectile] ENTITY (crossbow_bolt [895] at <2967.33 2120.63 94.6843>)
[this] TABLE
```
- [ ] Arc Titans causing crashes after giving ronin passive
      ```
    [02:29:14] [SCRIPT SV] [info] SCRIPT ERROR: [SERVER] Entity is null
	[02:29:14] [SCRIPT SV] [info]  -> titan.EndSignal( "OnDeath" )
	[02:29:14] [SCRIPT SV] [info] ai/_ai_emp_titans.gnut line[25]
## Todo
- [ ] Boost to summon a reaper. Reaper kills count for player.
- [ ] Setup exclusively server side voice lines for boss titan AI events
- [ ] MGL shoots ticks
- [ ] Cold war shoots batteries sometimes
- [ ] A-wall applies flat damage multiplier rather than adding amped flag
- [ ] Lock arc field ronin to core activation
- [ ] Add monarch heal rounds to heal score callback
- [ ] Add client side RUI for energy transfer health pool
- [x] Ronin with Thunderstorm passive is now an arc titan
- [ ] Nuke Core titan
	- [ ] Core ability is equivalent to a nuke eject explosion, however the titan does not get destroyed
	- [ ] thermal shield for tactical?
	- [ ] Stryder chassis
	- [ ] electric smoke as utility ability in addition to anti rodeo smoke.
	- [ ] deployable that uses the tether trap model and functions as a proximity mine
	- [ ] Cloak ability for tactical
	- [ ] Primary is a close range explosion? Potentially just punching but add an explosion on impact?
- [ ] Warp core titan
- [ ] Allow nuke eject to trigger before doomed state
- [ ] Smr missiles delayed immediately after firing. Stall in air then rapidly accelerate to deal more damage.
- [ ] Allow archer to lock onto players
- [ ] Smart pistol misses every shot while locked on
- [x] Lower probability of p2016 insta teamkilling. Add logic to fired projectile instead of the gun.
- [ ] Tighten eva8 spread. Shift fire offset to br akward. More ideal have the reticle be passed through a perspective transform to align with whatever plane the player is currently targetting. Projectiles shoot at an angle rather than just starting from an offset.
- [ ] A-wall no longer a deployable. Attach to player position and offset forward. Remain active for a set duration shrink size partially
- [x] Energy syphon causes monarch's shots to take hp from hit enemies and fill a meter. Shooting teammates will deplete this meter and refill their HP a respective amount
- [x] Arc grenade auto-hacks spectres
- [ ] Add the 30-30 with shattercaps. 3 body shots to a pilot to kill, headshots are oneshot (while adsed) if client side version of the mod is installed, use the actual 30-30 model. Otherwise use g2 model
- [ ] Legion gun functions similarly to updated devotion.
- [ ] Northstar shoots ion lasers at full railgun charge. Last pip takes slightly longer to charge? **NO** 
- [ ] Satchel becomes a proximity mine
- [ ] Mozambique projectiles grow with travel time
- [ ] Add guardian blocks after weapon callback loops
- [x] Spitfire shoots some kind of firestars
- [ ] Throw hands (I will not elaborate further on this)
- [x] Add dodge message announcement when upgrade 3 is triggered
- [x] CAR smg applies knockback to entities hit by shots if they are movable
- [ ] Ion gets shield mechanic similar to Asuka R# but uses energy instead of mana
- [ ] Give Monarch phase dash as an optional upgrade core
- [ ] Reapers can spawn ticks in attrition
- [ ] Northstar plasma railgun at max charge. Passively charges strength after firing. Shorter wait time causes less powerful shot
- [ ] Make Viper thrusters default flight speed for northstar hover and flightcore. Change viper thrusters to convert hover into a toggle ability with cooldown based on a multiplier of how long you were airborn for. Additionally allow dodging while airborn with viper thrusters
- [ ] Legion shoots thermite for bullets
- [ ] arc grenade hacks reapers. Look at leech_spectres function for implementation inspiration
- [ ] Give thunderbolt projectiles a gravitational field similar to grav stars (currently just have arc titan emp field applied to them will need to remove)
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