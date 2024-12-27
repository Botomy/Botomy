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
  multi_dash_cooldown: 1s,
```

```
const kill_reward_for_level = {
	1: 82,
	2: 114,
	3: 216,
	4: 317,
	5: 419,
	6: 520,
	7: 621,
	8: 723,
	9: 824,
	10: 926,
	11: 1027,
	12: 1129,
	13: 1230,
	14: 1331,
	15: 1433,
	16: 1534,
	17: 1636,
	18: 1737,
	19: 1838,
	20: 2000,
	21: 2000,
	22: 2000,
	23: 2000,
	24: 2000,
	25: 2000,
	26: 2000,
	27: 2000,
	28: 2000,
	29: 2000,
	30: 2000,
}
```

XP reward does not change beyond level 20 because there are no additional buffs given - a level 30 player will theoretically be just as easy to kill when they were at level 20.
The level difference bonus/penalty still applies (see below).

There is a 3.33% bonus/penalty for every level difference in the opponent you kill starting with a level difference of 2.

e.g.

player level: 1
enemy level: 2
0% bonus

player level: 1
enemy level: 3
6.66% bonus

player level: 3
enemy level: 1
6.66% penalty

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

There are 30 levels. Players gain a skill point for each new level reached up to level 20.

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
			"20":150000,
			"21": 165375,
			"22": 181500,
			"23": 198375,
			"24": 216000,
			"25": 234375,
			"26": 253500,
			"27": 273375,
			"28": 294000,
			"29": 315375,
			"30": 337500
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
