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

## Getting Started

### Option 1: In-Game Editor (Basic)

The game includes a built-in JavaScript code editor where you can write and run your bot code directly.

1. Launch Botomy
2. Click "Script Mode"
3. Start coding your bot in JavaScript

No additional setup required!

### Option 2: External Server (Advanced)

For more advanced development, you can run your bot as an external API server in your preferred language:

- [TypeScript Starter](https://github.com/botomy/botomy-node-starter)
- [Python Starter](https://github.com/botomy/botomy-python-starter)

Your server must:

- Accept POST requests at the root endpoint (`/`)
- Accept level data in the request body
- Return an array of moves

To connect your server:

1. Launch Botomy
2. Click "API Mode" to enable external connections
3. Make sure your server is running on port 3000

:::tip
New to coding? Start with the in-game editor - it's the easiest way to begin!
:::

See the [Quickstart Tutorial](/docs/getting-started/quickstart-tutorial) for next steps.
