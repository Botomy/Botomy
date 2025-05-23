---
sidebar_position: 4
---

# Survival

How many stages can you complete? Each stage gets progressively harder.

:::tip
Levelling is in play so level up as fast as you can.
:::

The game ends when all players are dead.

## Important data

### Map

```
size: 2400x2400
```

### Player

```
  kill: { xp_points: 60 * (some complicated multiplier based on the level of the player that was killed - 6x at level 20) }
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
  "max_xp": 70000,
  "max_attack_level": 10,
  "max_speed_level": 5,
  "max_health_level": 8,
  "attack_increase": 7,
  "speed_increase": 30,
  "health_increase": 30,
  "bands": {
    "1":0,
    "2":700,
    "3":1575,
    "4":2800,
    "5":4375,
    "6":6300,
    "7":8575,
    "8":11200,
    "9":14175,
    "10":17500,
    "11":21175,
    "12":25200,
    "13":29575,
    "14":34300,
    "15":39375,
    "16":44800,
    "17":50575,
    "18":56700,
    "19":63175,
    "20":70000,
  }
```

### Wolves

```
  weapon: 10
  hp: 65
  speed: 20000
  xp_points: 80
```

### Ghouls

```
  weapon: 30
  hp: 100
  speed: 15000
  xp_points: 100
```

### Tiny's

```
  weapon: 50
  hp: 50
  speed: 50000
  xp_points: 300
```

### Minotaurs

```
  weapon: 50
  hp: 400
  speed: 10000
  xp_points: 600
```
