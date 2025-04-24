---
sidebar_position: 1
---

# Enemies

The `enemies` array contains information about NPC enemies:

```json
[
  {
    "id": "Ghoul1",        // Unique enemy identifier
    "type": "ghoul",         // Enemy type (wolf/ghoul/minotaur/tiny)
    "position": {           // Current position on map
      "x": 500,
      "y": 600
    },
    "health": 100,          // Current health points
    "attack_damage": 30,   // Damage dealt by attacks
    "is_zapped": false,    // Affected by speed zapper
    "is_frozen": false,    // Frozen by ice attacks
    "is_pushed": false,    // Being pushed back
    "direction": "left",   // Facing direction
    "points": 100         // XP awarded when killed
  }
]
```

## Enemy Types

- [Wolf](./wolf/wolf.md) - Fast melee attacker
- [Ghoul](./ghoul/ghoul.md) - Balanced medium-range attacker
- [Minotaur](./minotaur/minotaur.md) - Heavy hitting tank
- [Tiny](./tiny/tiny.md) - Small but deadly punch specialist

:::tip General Strategy

- Use speed zappers to slow down fast enemies
- Use rings to cloak out of trouble or sneak up on enemies
- Freeze is effective against all enemy types
- Shockwave can push enemies away to create space
- Level up as quickly as you can
  :::
