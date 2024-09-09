---
sidebar_position: 2
---

# Level Data

## game_info

```
  game_info: {
    map: <name>,
    game_type: <rpg/racing>,
    state: <STARTING/STARTED/ENDING/ENDED/MATCH_COMPLETED>,
    time_left_s, // time left in the round in secs
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
    attack_damage,
    is_cloaked,
    is_shield_ready,
    shield_raised,
    direction: <"left"/"right">,
    is_zapping,
    is_attacking,
    is_zapped,
    is_boosted,
    is_dashing,
    is_dash_ready,
    is_colliding,
    speech,
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
      attack_damage,
      shield_raised,
      direction: <"left"/"right">,
      is_attacking,
      is_zapping,
      is_zapped,
      is_boosted,
      is_dashing,
      speech,
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
      attack_damage,
      is_zapped,
      direction: <left/right>,
    }
  ]
```

## obstacles

`x,y` coordinates of tiles that are obstacles on the map.
Each object is 48x48.

```
  obstacles: [
    {
      x,
      y,
    },
    {
      x,
      y,
    },
    ...
  ]
```

## stats

```
  stats: {
    "<player_id_1>": {
      score,
      kills,
      deaths,
      kd_ratio,
    }
    "<player_id_2>": {
      score,
      kills,
      deaths,
      kd_ratio,
    }
  }
```
