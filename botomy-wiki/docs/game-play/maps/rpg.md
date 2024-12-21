---
sidebar_position: 1
---

# RPG

The player with the most xp at the end of the round wins.

Increase your xp by killing things and collecting coins.

As your xp increases, you reach new levels. Each new level comes with a skill point you can redeem for - attack, speed, or health.

:::info
There are limits to how much you can max each skill tree
:::

If you are killed, you will not lose xp.

## Important data

### Round Time

```
  duration: 30, //mins
```

### Map

```
size: varies
```

### Player

```
  kill: { xp_points: *see below }
  death: { xp_points: 0 }
  damage: 15
  starting_hp: 100
  starting_speed: 415
  attack_slowdown: 0.6, // move at 60% speed while attacking
  dash_speed: 1500,
  dash_duration: 0.1s,
  dash_cooldown: 0.25s,
  multi_dash_limit: 2,
  multi_dash_cooldown: 4s,
```

```
const kill_reward_for_level = {
	1: 82,
	2: 95,
	3: 109,
	4: 126,
	5: 144,
	6: 166,
	7: 191,
	8: 220,
	9: 253,
	10: 291,
	11: 335,
	12: 386,
	13: 444,
	14: 511,
	15: 587,
	16: 676,
	17: 777,
	18: 894,
	19: 1029,
	20: 1184
}
```

### Coins

```
  gold: {
    xp_points: 200
  },
```

### Big Potions

```
  heal: 1.0, // 100% of health
  max_carry: 6,
  xp_points: 12,
```

### Speed Zappers

```
  duration: 2.0, // secs
  slowdown: 0.3, // 30% of speed (i.e. movement is 70% of speed)
  max_slowdown: 0.3, // 90% of speed (i.e. movement is 10% of speed)
  max_carry: 5,
  xp_points: 12,
```

### Rings

```
  duration: 5.0, // secs
  max_carry: 5,
  xp_points: 12,
```

### Shield

```
  duration: 1.0, // secs
  drain: 0.4, // secs (triggered on hit or after `duration`)
  cooldown: 5.0, // secs
```

### Levelling

```
  "max_levels": 20,
  "max_xp": 150000,
  "max_attack_level": 10,
  "max_speed_level": 5,
  "max_health_level": 8,
  "attack_increase": 7,
  "speed_increase": 25,
  "health_increase": 30,
  "bands": {
			"1":0,
			"2":1500,
			"3":3375,
			"4":6000,
			"5":9375,
			"6":13500,
			"7":18375,
			"8":24000,
			"9":30375,
			"10":37500,
			"11":45375,
			"12":54000,
			"13":63375,
			"14":73500,
			"15":84375,
			"16":96000,
			"17":108375,
			"18":121500,
			"19":135375,
			"20":150000
  }
```

### Wolves

```
  weapon: 10
  hp: 30
  speed: 330
  xp_points: 80
```

### Ghouls

```
  weapon: 30
  hp: 100
  speed: 250
  xp_points: 100
```

### Tiny's

```
  weapon: 50
  hp: 50
  speed: 830
  xp_points: 300
```

### Minotaurs

```
  weapon: 50
  hp: 400
  speed: 165
  xp_points: 600
```
