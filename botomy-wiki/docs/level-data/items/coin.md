---
sidebar_position: 1
---

# Coin

Coins are collectible items that award xp points when picked up.

![Coin](./images/coin.gif)

```json
{
  "id": "Coin1",           // Unique item identifier
  "type": "coin",         // Item type
  "position": {           // Current position on map
    "x": 100,
    "y": 200
  },
  "value": 200,          // Coin value (same as points)
  "points": 200          // XP points awarded when collected
}
```
