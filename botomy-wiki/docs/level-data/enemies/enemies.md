---
sidebar_position: 4
---

# Enemies

The `enemies` array contains information about NPC enemies:

```json
[
  {
    "id": "Tiny1",         // Unique enemy identifier
    "type": "tiny",          // Enemy type (wolf/ghoul/minotaur/tiny)
    "position": {            // Current position on map
      "x": 500,
      "y": 600
    },
    "health": 50,           // Current health points
    "attack_damage": 25,    // Damage dealt by attacks
    "is_zapped": false,     // Affected by speed zapper
    "is_frozen": false,     // Frozen by ice attacks
    "is_pushed": false,     // Being pushed back
    "direction": "left",    // Facing direction
    "points": 100          // XP awarded when killed
  }
]
```

## Enemy Types

- `wolf` - Fast melee attacker with little health
- `ghoul` - Average attacker
- `minotaur` - Big monster that gives as good as it gets
- `tiny` - Quick and agile with a powerful punch

:::tip
Different enemy types require different strategies - wolves are fast but weak, while minotaurs are slow but tough
:::
