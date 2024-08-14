---
sidebar_position: 2
---

# Level Data

## game_info

```
  game_info: {
    map: <name>,
    game_type: <rpg/racing>
  }
```

## items

```
  items: [
    {
      type: "coin",
      id,
      position: {x, y},
      value,
      points,
    },
    {
      type: "feather",
      id,
      position: {x, y},
      value, // speed boost percentage
      duration, // in seconds
    },
    {
      type: "big_potion",
      id,
      position: {x, y},
      value, // not used
    },
    {
      type: "speed_zapper",
      id,
      position: {x, y},
      value, // speed zap percentage
      duration, // in seconds
    },
    {
      type: "ring",
      id,
      position: {x, y},
      duration, // in seconds
    },
  ]
```

## own_player

```
  own_player: {
    id,
    type: "player",
    display_name,
    position: {x, y},
    items: [
      big_potions: [ {value} ],
      feathers: [ {value, duration }],
      speed_zappers: [ { value, duration }],
      rings: [ { duration }],
    ],
    max_health,
    health,
    is_cloaked,
    is_shield_ready,
    shield_raised,
    direction: <"left"/"right">,
    is_attacking,
    is_zapped,
    is_boosted,
    score,
    levelling: { // only in fight world
      level,
      available_skill_points,
      attack, // redeemed attack points
      speed, // redeemed speed points
      health, // redeemed health points
    }
  }
```

## players

```
  players: [
    {
      id,
      type: "player",
      display_name,
      position: {x, y},
      health,
      shield_raised,
      direction: <"left"/"right">,
      is_attacking,
      is_zapped,
      is_boosted,
      score,
      levelling: { // only in fight world
        level,
      },
    }
  ]
```

## enemies

```
  enemies: [
    {
      type: <wolf/ghoul/minotaur/tiny>
      id,
      position: {x, y},
      health,
      is_zapped,
    }
  ]
```
