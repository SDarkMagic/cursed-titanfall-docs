---
tags:
  - titanfall
  - cursed-titanfall
  - modding
  - squirrel
  - scripts
---
# Framework
-----------------
Builds off of the features implemented by [[Core]] and adds a majority of the callback registration functions and relevant implementations that are used by the rest of the mod.
# Weapon Callbacks
Several weapons have had callbacks for projectile collision or player primary attack added to them. The name scheme for the callback registration functions is `AddCallback_OnProjectileCollision_weapon_<weapon_internal_name>` and `AddCallback_OnPrimaryAttackPlayer_weapon_<weapon_internal_name>` where `<weapon_internal_name>` is the unique identifier for the weapon, such as `epg` or `softball`
Additionally, some of the internal weapon behaviors have been modified to allow certain callbacks to work on them. For example, the Spitfire (`mp_weapon_lmg`) is now a projectile weapon that uses the `FireWeaponGrenade` method to shoot.

A full list of the available registration functions is as follows:
- `AddCallback_OnPrimaryAttackPlayer_weapon_epg`
- `AddCallback_OnProjectileCollision_weapon_epg`
- `AddCallback_OnPrimaryAttackPlayer_weapon_defender`
- `AddCallback_OnPrimaryAttackPlayer_weapon_softball`
- `AddCallback_OnProjectileCollision_weapon_softball`
- `AddCallback_OnPrimaryAttackPlayer_weapon_wingman`
- `AddCallback_OnProjectileCollision_weapon_wingman`
- `AddCallback_OnPrimaryAttackPlayer_weapon_lmg`
- `AddCallback_OnBulletHit_weapon_lmg` (Please note this function passes a weapon `entity` and a `WeaponBulletHitParams` object )
- `AddCallback_OnWeaponPrimaryAttackPlayer_weapon_alternator_smg`
- `AddCallback_OnWeaponReload_weapon_alternator_smg`
- `AddRandomEventCallback_FragGrenade`