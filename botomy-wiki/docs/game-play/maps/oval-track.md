---
sidebar_position: 3
---

# Oval Track

This is a racing game!

First to complete 3 laps wins the round.

Each game is 3 rounds.

## Important data

### Round

```
  laps: 3,
  rounds: 3,
```

### Player

```
  damage: 34
  starting_hp: 100
  starting_speed: 30000
  attack_slowdown: 0.8, // move at 80% speed while attacking
```

### Feathers

```
  duration: 2.0, // secs
  boost: 1.0, // 100% of your current speed (i.e. double speed)
  max_carry: 5,
  xp_points: 12,
```

### Big Potions

```
  heal: 1.0, // 100% of health
  max_carry: 6,
  xp_points: 12,
```

### Shield

```
  duration: 1.0, // secs
  drain: 0.4, // secs (triggered on hit or after `duration`)
  cooldown: 5.0, // secs
```
