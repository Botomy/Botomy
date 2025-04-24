---
sidebar_position: 1
---

# Install

## Download the app

Get started by **[downloading](https://store.steampowered.com/app/3566430/Botomy)** and installing the app from [Steam](https://store.steampowered.com/about/).

### Supported Platforms

- MacOS Universal 64 bit
- Windows x86_64
- Linux x86_64

## Set up your local development environment

Your "game controller" is an API server running outside of the game. The server must:

- Accept POST requests at the root endpoint (`/`)
- Accept level data in the request body
- Return an array of moves

Set up your own API server or choose one of our official starter projects to begin coding your bot.

### TypeScript

```typescript
// Example endpoint
app.post('/', (req, res) => {
  const levelData = req.body;
  const moves = play(levelData);
  res.json(moves);
});
```

https://github.com/botomy/botomy-node-starter

### Python

```python
# Example endpoint
@app.post("/")
async def handle_moves(level_data: dict):
    moves = play(level_data)
    return moves
```

https://github.com/botomy/botomy-python-starter

:::tip
Don't see a starter that works for you? Join our [Discord server](https://discord.gg/TTdkaA63zX) and we'll be happy to spin one up for you!
:::

See the [Quickstart Tutorial](/docs/getting-started/quickstart-tutorial) for next steps.
