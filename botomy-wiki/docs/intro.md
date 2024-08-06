---
sidebar_position: 1
---

# Tutorial Intro

Let's discover **Botomy in less than 5 minutes**.

## Getting Started

Get started by **[downloading](https://botomy.vercel.app) and installing the app**.

Or **try Botomy immediately** in the **[browser](https://botomy.vercel.app/dist/web/index.html)**.

### Supported Platforms

- MacOS
- Windows
- HTML5 (limited support - use at your own risk)

## Practice Offline

Select "Offline Pratice" and start the "Tutorial" map

## The `play` function

Your script must define a `play` function. This function is called on every frame (mostly).

The function should return the list of moves (i.e. key presses) that the bot should follow.

## Movement

If you want the bot to move left, then `return ["move_left]`. If you want the bot to move diagonnally up and right, then `return ["move_up", "move_right"]`.

## Actions

### Attack

`return ["attack"]`

### Speak

`return [{"speak": "Hello there"}]`

### Use Items

`return [{"use": "feather"}]`

### Redeeming Skill Points

`return [{"redeem_skill": "attack"}]`
