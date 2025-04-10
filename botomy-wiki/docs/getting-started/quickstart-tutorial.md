---
sidebar_position: 2
---

# Quickstart Tutorial

## Start a game

Select **Practice**

## Download Starter Projects

### Node.js Starter

```bash
git clone https://github.com/Brokkli-Labs/botomy-node-starter
cd botomy-node-starter
npm install
npm start
```

A server on port 3000 and calls the `play` function in `src/play.ts`

Modify `src/play.ts` to program your bot.

:::tip Node.js Features
The Node.js starter includes:

- Express server setup
- Basic bot logic template
- TypeScript definitions for game data
  :::

### Python Starter

```bash
git clone https://github.com/Brokkli-Labs/botomy-python-starter
cd botomy-python-starter
pip install -r requirements.txt
uvicorn main:app --port 3000 --reload
```

A FastAPI server will start on port 8000 and calls the `play` function in `play.py`

Modify `play.py` to program your bot.

:::tip Python Features
The Python starter includes:

- FastAPI server setup
- Basic bot logic template
- Type hints for game data
  :::

:::tip Next Steps

- Review [Basic Gameplay](/docs/game-play/basic-gameplay)
- Join our [Discord](https://discord.gg/TTdkaA63zX) for help
  :::

## Use the API play mode

Select the `ApiCall` tab (probably already selected).

Press "Run" to start executing the default script. You should see your character say "Hello Botomy!"
