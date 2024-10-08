# Titans
------------
The overall philosophy behind the majority of the titan changes is to further incentivize players to lean into their preferred playstyles and respective rolls. For example, to encourage players to play more aggressively and up close, performing an execution with ronin will allow the player to heal slightly. 
## Features
----------------
### Monarch
- Activating upgrade core 3 may attempt to drop a reaper onto the player's location. This will be warned with both a text popup **AND** Viper's voiceline of "Dodge this" playing. You *must* use your dash or be sprinting at time of activation in order to avoid being crushed
- The core 2 upgrade, rearm and reload, now gives the player northstar's hover ability instead of the rearm ability
- The core 1 upgrade, arc rounds, now comes equipped with the gunrunner property that some SMGs are capable of equipping. This allows you to spring while firing your primary weapon as Monarch.
- The core 1 upgrade, missile racks, now includes the abilities that could be previously obtained from the core 2 rearm and reload upgrade. This includes both the faster rearm speed as well as a slightly faster reload speed for your primary weapon
- The core 1 upgrade, energy transfer, now additionally gives monarch a reserve health pool with an equal value to your max health. This pool will increase in size if you use the core 3 upgrade enhanced chassis. This pool does not directly affect monarch's health bar, however if it has any points in it, shooting a teammate's titan with your primary weapon will now allow you to heal them. The health points in this pool are refilled by dealing damage to enemies with monarch's primary weapon. Additionally, the health value restored to friendly titans is loosely based on the amount of damage the shot would do, meaning you can get crit heals by shooting friendly titan's weak points
### Ion
- Laser tripwire now lasts for 30 seconds before despawning
- Damage from energy weapons or electrical/arc sources is now absorbed and recharges Ion's energy meter
- The `Split Shot Power` aegis upgrade now causes damaging enemies with the splitter rifle to refill Ion's energy
- Ion no longer uses ammo. All shots fired from the primary weapon will instead drain from her energy pool. This may need to be later balanced further as it was designed around the FD aegis upgrades
- Maintain default movement speed during the startup of laser core. While in the firing state for laser core, you are now able to use your dashes.
### Tone
- Burst shot mod now has a max burst size of 12 shots
- A small sonar pulse is created at the user's position when firing the tracker cannon. This can be used to quickly acquire locks when surrounded by multiple enemies
### Scorch
- Scorch will no longer take damage when standing in his own fire, regardless of the kit you have equipped
- The tempered plating kit now provides scorch with shield regeneration when standing in your own fire. **Please note:** You can still take damage from your incendiary traps explosion if using them to recharge shields. This explosion has a hitbox at both the start and end of the traps burn time
- When becoming doomed for the first time, scorch will now automatically undoom and regen two bars of health while creating a fiery explosion around himself. **Note**: similar to the gas trap explosions, the explosion created from this ability can damage you both on startup and when it's ending. Moving away from the center of this fire source is recommended. 
### Northstar
- The hover movement speed that was previously provided by the viper thruster's kit is now the default movement speed when using hover
- Viper thrusters now converts the hover ability into a toggle with a max flight time of 30 seconds.
- Player northstar's gain a personal cloak drone that follows them for 30 seconds after using electric smoke antirodeo counter measures. Functions very similarly to the cloak drones in Frontier Defense
- Equipping the Enhanced Payload kit now additionally causes flightcore to fire cluster missiles
- The threat optics kit now additionally adds an increased critical damage multiplier to northstar's plasma railgun. This will stack with the frontier defense crit damage upgrade multiplicatively.
### Ronin
- The thunderstorm kit now additionally gives ronin an arc field similar to what the arc titans from frontier defense have
- Performing an execution on an enemy titan as ronin will now give the player performing the execution a battery upon completion, similar to how monarch's energy thief kit works
- Pressing guard right before being hit by an enemy titan melee will allow you to parry. Depending on the amount of core charge you have, the attacker will be force executed. You need 10% core charge for every cell of health the attacker has, which will be consumed upon terminating them. Regardless of core charge, all damage from the melee attack will be negated. *The forced execution mechanic does not work on boss titans. You will only negate the damage from their attacks*
### Legion
- Legion takes approximately 1/3 less damage from all damage sources as opposed to vanilla
- Additionally, taking damage as legion, either to health **or** shields will refill the predator cannon ammo based on the amount of damage taken. More ammo will be refunded if you take damage to your shields