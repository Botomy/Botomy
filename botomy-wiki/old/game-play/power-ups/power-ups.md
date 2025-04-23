# Power Ups

## Bomb

```
	"max_damage": 200,
	"damage_factor": 2.5, // factor of the player's current attack damage
	"cooldown": 1.5,
```

:::warn
Bombs can do self damage. Be careful after you've dropped a bomb.
:::

## Freeze

```
	"cooldown": 1.5,
	"duration": 1.0, // how long an enemy will be frozen for (sec)
	"max_damage": 20,
	"damage_factor": 0.33, // factor of the player's current attack damage
	"damage_absorption_factor": 0.3, // how much damage is asborbed by the ice when frozen (i.e. when frozen, damage is received at 70%)
```

## Shockwave

```
	"duration": 0.2,
	"cooldown": 1.5,
	"speed": 1500,
	"max_damage": 15,
	"damage_factor": 0.2, // factor of the player's current attack damage
```
