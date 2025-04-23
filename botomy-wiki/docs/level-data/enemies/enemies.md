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

### Wolf

- Fast melee attacker
- Low health but high speed
- Attack rate is higher than other enemies
- Best strategy: Use your shield

**Stats:**

- Health: 30
- Attack Damage: 10
- XP Points: 80

### Ghoul

- Balanced attacker with medium stats
- Stronger than a lvl 1 player
- Best strategy: Level up, use shields and potions

**Stats:**

- Health: 100
- Attack Damage: 30
- XP Points: 100

### Minotaur

- Heavy hitter
- High health and high damage
- Slow movement speed
- Worth more XP points
- Best strategy: Hit them when their arms are raised

**Stats:**

- Health: 400
- Attack Damage: 50
- XP Points: 600

### Tiny

- Small but deadly
- Powerful punch attack
- Keeps it's distance if you're looking at it
- Best strategy: Sneak attacks work best

**Stats:**

- Health: 50
- Attack Damage: 50
- XP Points: 300

:::tip

- Use speed zappers to slow down fast enemies
- Use rings to cloak out of trouble or sneak up on enemies
- Freeze is effective against all enemy types
- Shockwave can push enemies away to create space
- Level up as quickly as you can
  :::
