---
sidebar_position: 1
---

# Level Data

The `level_data` object contains the following top-level properties:

```json
{
  "game_info": {},      // Current game state information
  "own_player": {},     // Your player's information
  "items": [],          // Collectible items on the map
  "players": [],        // Other players in the game
  "enemies": [],        // NPC enemies
  "obstacles": [],      // Static obstacles and terrain
  "hazards": [],        // Dynamic hazards like bombs and icicles
  "stats": {}           // Match statistics
}
```

Each property provides different aspects of the current game state. See the specific sections for detailed information about each type:

- [Game Info](./game-info/game-info.md)
- [Own Player Info](./own-player/own-player.md)
- [Player Info](./players/players.md)
- [Enemy Info](./enemies/enemies.md)
- [Item Info](./items/items.md)
- [Obstacle Info](./obstacles/obstacles.md)
- [Hazard Info](./hazards/hazards.md)
- [Stats Info](./stats/stats.md)
