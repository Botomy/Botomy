---
sidebar_position: 6
---

# Obstacles

The `obstacles` array contains the x,y coordinates of obstacle tiles on the map:

```json
{
  "obstacles": [
    {
      "x": 48,    // X coordinate of obstacle tile
      "y": 96     // Y coordinate of obstacle tile
    },
    {
      "x": 96,    // Each obstacle tile is 48x48 pixels
      "y": 96
    }
  ]
}
```

:::tip
Obstacles are static 48x48 tiles that cannot be moved or destroyed during gameplay
:::
