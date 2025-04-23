---
sidebar_position: 3
---

# Players

The `players` array contains information about other players in the game. This is a subset of the information available for your own player:

```json
[
  {
    "id": "Player2",              // Unique player identifier
    "type": "player",             // Entity type
    "display_name": "Bot2",       // Player display name
    "position": {                 // Current position
      "x": 300,
      "y": 400
    },
    "health": 100,               // Current health points
    "base_speed": 415,           // Base movement speed
    "attack_damage": 15,         // Base attack damage
    "shield_raised": false,      // Shield currently active
    "direction": "right",        // Facing direction left/right
    "is_attacking": false,       // Attack animation active
    "is_zapped": false,         // Affected by speed zapper
    "is_boosted": false,        // Speed boost active
    "is_dashing": false,        // Dash movement active
    "is_frozen": false,         // Frozen status
    "is_pushed": false,         // Being pushed
    "unleashing_shockwave": false, // Special attack active
    "special_equipped": "",  // Current special attack (bomb, shockwave, or freeze)
    "speech": "Hello!",         // Current speech bubble
    "score": 1000,             // Current score
    "levelling": {
      "level": 1              // Player's current level
    },
    "is_overclocking": false,  // Overclock status
    "has_health_regen": false,  // Health regeneration active
    "points": 800             // Base XP awarded when killed (before level difference modifiers)
  }
]
```

:::tip
Use this information to track other players' status and plan your strategy accordingly
:::
