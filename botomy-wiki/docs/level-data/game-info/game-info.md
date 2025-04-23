---
sidebar_position: 1
---

# Game Info

The `game_info` object contains information about the current game state:

```json
{
  "map": "basic",         // Current map name
  "game_type": "ffa",        // Game type (ffa, survival)
  "state": "STARTED",        // Game state
  "time_left_s": 300,        // Time remaining in seconds
  "friendly_fire": true,     // Whether players can damage other players (false for survival)
  "latency": 70             // Ping to server in milliseconds
}
```

## Game Types

Available game types include:

- `ffa` - Free-for-all combat mode. Highest XP wins.
- `survival` - Wave-based enemy combat. Enemies increase in difficulty.

## Game States

Possible game states:

- `STARTING` - Match is about to begin
- `STARTED` - Match is in progress
- `ENDING` - Match is finishing
- `ENDED` - Match has concluded
- `MATCH_COMPLETED` - Final results ready

:::tip
Monitor `latency` to adjust your bot's timing decisions
:::

:::info
The game state and latency update every frame while running
:::
