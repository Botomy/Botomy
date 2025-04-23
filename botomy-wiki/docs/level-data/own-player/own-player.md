---
sidebar_position: 2
---

# Own Player

The `own_player` object contains detailed information about your player:

```json
{
  "id": "Player1",              // Unique player identifier
  "type": "player",             // Entity type
  "display_name": "Protobot",       // Player display name
  "position": {                 // Current position
    "x": 100,
    "y": 200
  },
  "items": {                    // Inventory count
    "big_potions": 1,
    "speed_zappers": 0,
    "rings": 2
  },
  "max_health": 100,            // Maximum health points
  "health": 75,                // Current health points
  "base_speed": 400,           // Base movement speed
  "attack_damage": 25,         // Base attack damage
  "is_cloaked": false,         // Invisibility status
  "is_shield_ready": true,     // Shield ability available
  "shield_raised": false,      // Shield currently active
  "direction": "right",        // Facing direction
  "is_attacking": false,       // Attack animation active
  "is_zapped": false,         // Affected by speed zapper
  "is_boosted": false,        // Speed boost active
  "is_dashing": false,        // Dash movement active
  "is_dash_ready": true,      // Dash ability available
  "is_zap_ready": true,       // Speed zap ability available
  "is_colliding": false,      // Collision detection
  "collisions": [             // Active collisions
    {
      "relative_pos": { "x": 10, "y": 0 },
      "type": "bomb"
    }
  ],
  "is_frozen": false,         // Frozen status
  "is_pushed": false,         // Being pushed
  "unleashing_shockwave": false, // Special attack active
  "is_special_ready": true,   // Special ability available
  "speech": "Hello!",         // Current speech bubble
  "score": 1000,             // Current score
  "levelling": {             // Level progression
    "level": 3,
    "available_skill_points": 1,
    "attack": 2,             // Attack skill points used
    "speed": 1,              // Speed skill points used
    "health": 0              // Health skill points used
  },
  "is_overclocking": false,  // Overclock status
  "overclock_duration": 0,   // Remaining overclock time
  "has_health_regen": true,  // Health regeneration active
  "points": 800             // Base XP awarded when killed (before level difference modifiers)
}
```

:::tip
Monitor status flags like `is_dash_ready` and `is_special_ready` to time your abilities effectively
:::

:::info
The `points` value represents the base experience points (XP) that other players will receive for eliminating you. This base value is modified by level differences between players.
:::
