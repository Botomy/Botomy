---
sidebar_position: 4
---

# Ring

Rings grant temporary cloak when used.

```json
{
  "id": "Ring1",        // Unique item identifier
  "type": "ring",       // Item type
  "position": {         // Current position on map
    "x": 100,
    "y": 200
  },
  "duration": 5,       // Invisibility duration in seconds
  "points": 12         // XP points awarded when collected
}
```

:::tip
While cloaked:

- Enemies and players cannot see you
- Shields cannot be used
- Attacking briefly uncloaks you
  :::
