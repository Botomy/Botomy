---
sidebar_position: 5
---

# Items

The `items` array contains information about collectible items on the map:

```json
[
  {
    "id": "Coin1",           // Unique item identifier
    "type": "coin",           // Item type
    "position": {             // Current position on map
      "x": 100,
      "y": 200
    },
    "value": 200,            // Coin value
    "points": 200            // XP points awarded
  },
  {
    "id": "BigPotion1",
    "type": "big_potion",
    "position": {
      "x": 300,
      "y": 400
    },
    "value": 100,           // Percentage of health regained when used
    "points": 12            // XP points awarded
  },
  {
    "id": "SpeedZapper1",
    "type": "speed_zapper",
    "position": {
      "x": 500,
      "y": 600
    },
    "value": 0.5,           // Speed reduction percentage
    "duration": 5,          // Effect duration in seconds
    "points": 12            // XP points awarded
  },
  {
    "id": "Ring1",
    "type": "ring",
    "position": {
      "x": 700,
      "y": 800
    },
    "duration": 5,         // Cloak duration in seconds
    "points": 12          // XP points awarded
  }
]
```

## Item Types

- `big_potion` - Restores health to maximum
- `ring` - Grants temporary invisibility
- `speed_zapper` - Creates lightning storm that slows enemies
- `chest` - Contains random power ups
- `power_up` - Grants special abilities

:::tip
Items disappear when collected and respawn after a delay
:::
