---
sidebar_position: 2
---

# Coin World

The player with the most points at the end of the round wins.

If you die, you lose points.

If you kill someone, you can collect the coins they drop.

## Important data

### Map

```
size: 8640x4320
```

### Round Time

```
  duration: 15, //mins
```

### Player

```
  kill: { points: 0 }
  death: { points: -200 }
  weapon_damage: 15
```

### Coins

```
  red: {
    points: 14
  },
  blue: {
    points: 23
  },
  gold: {
    points: 36
  },
```

### Feathers

```
  duration: 2.0, // secs
  boost: 1.0, // 100% of your current speed (i.e. double speed)
  max_carry: 5,
  points: 0,
```

### Big Potions

```
  heal: 1.0, // 100% of health
  max_carry: 6,
  oints: 0,
```

### Speed Zappers

```
  duration: 2.0, // secs
  slowdown: 0.3, // 30% of speed (i.e. movement is 70% of speed)
  max_slowdown: 0.9, // 90% of speed (i.e. movement is 10% of speed)
  max_carry: 5,
  points: 0,
```

### Rings

```
  duration: 1.0, // secs
  max_carry: 5,
  points: 0,
```

### Shield

```
  duration: 1.0, // secs
  drain: 0.4, // secs (triggered on hit or after `duration`)
  cooldown: 5.0, // secs
```

### Levelling

```
  N/A
```
