---
sidebar_position: 3
---

# Speed Zapper

Speed zappers create a lightning storm that slows down enemies caught in its radius.

```json
{
  "id": "Zapper1",        // Unique item identifier
  "type": "speed_zapper", // Item type
  "position": {           // Current position on map
    "x": 100,
    "y": 200
  },
  "value": 0.3,          // Speed reduction - i.e. 30%
  "duration": 2,         // Effect duration in seconds
  "points": 12          // XP points awarded when collected
}
```

:::tip

- Creates a lightning storm with radius 475
- Lightning storm lasts for 0.8 seconds
- Reduces target speed by 30%
- Slowdown effect lasts for 2 seconds on hit targets
  :::
