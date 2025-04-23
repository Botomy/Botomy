---
sidebar_position: 7
---

# Hazards

Hazards are things that can hurt you - bombs, icicles, lightning storms, etc.

The `hazards` array contains information about active hazards on the map:

```json
[
  {
    "id": "Bomb1",              // Unique hazard identifier
    "type": "bomb",             // Type of hazard
    "position": {               // Position on map
      "x": 100,
      "y": 200
    },
    "attack_damage": 50,        // Damage dealt when triggered
    "status": "charging",       // Current state (charging/active/idle)
    "owner_id": "Player1"       // ID of player who created hazard
  }
]
```

## Hazard Types

- `bomb` - Explosive device that deals area damage
- `icicle` - Fired by players that freezes enemies and players impact
- `lightning_storm` - Created by speed_zapper, slows affected players

:::tip
Monitor hazard status to time your movements - dodge during "charging", avoid during "active"
:::
