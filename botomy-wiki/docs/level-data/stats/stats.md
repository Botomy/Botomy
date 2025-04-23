---
sidebar_position: 8
---

# Stats

The `stats` object contains match statistics for each player:

```json
{
  "Player1": {
    "score": 100000,        // Total xp score
    "kills": 5,             // Total kills
    "deaths": 2,            // Total deaths
    "coins": 10,            // Coins collected
    "kd_ratio": 2.5,        // Kill/death ratio
    "kill_streak": 3,       // Current kill streak
    "overclocks": 1,        // Total of overclocks achieved
    "xps": 200,             // Current xp/s
    "wolf_kills": 2,        // Wolves eliminated
    "ghoul_kills": 1,       // Ghouls eliminated
    "tiny_kills": 0,        // Tiny enemies eliminated
    "minotaur_kills": 1,    // Minotaurs eliminated
    "player_kills": 1,      // Other players eliminated
    "self_destructs": 0     // Total self-destructs
  },
  "Player2": {
    "score": 85000,
    "kills": 3,
    "deaths": 4,
    "coins": 5,
    "kd_ratio": 0.75,
    "kill_streak": 0,
    "overclocks": 0,
    "xps": 150,
    "wolf_kills": 1,
    "ghoul_kills": 1,
    "tiny_kills": 1,
    "minotaur_kills": 0,
    "player_kills": 0,
    "self_destructs": 1
  }
}
```

:::tip
Use these stats to track performance and adapt your strategy during matches
:::
