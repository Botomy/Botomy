---
sidebar_position: 1
---

# Basic Gameplay

## Play modes

To enable a play mode, select the tab and press **RUN**. You can stop execution at any time by pressing **STOP**.

:::info
You can only run one mode at a time. Pressing **RUN** in one mode will stop execution in another mode.
:::

There are two supported play modes (see below):

### ApiCall

This mode makes a POST call to the specificed url. It passes in a `level_data` object and expects a list of moves returned.

:::info

If the previous call has not returned, the API will not be called. The specified API will be called by the game engine at most every frame.

:::

:::tip
Using this mode allows you to use any language or libraries you want. Your imagination is the limit here (and maybe your programming skills)
:::

### Manual

This mode allows you to use keyboard input to control your character.

:::warn
This mode can get very boring.
:::

## Basic Movement

### move_to

| <small>**script**:`move_to` **manual**:`arrow keys`</small>

Your player will move to a given x,y target.
`move_to: {x, y}`

e.g.
`return [{"move_to": {"x": 10, "y": 20}}]`

:::info

Your player will navigate to the target using basic astar pathfinding (built into the engine)

:::

## Basic Combat

### attack

| <small>**script**:`attack` **manual**:`space bar`</small>

This will cause the character to attack in the direction it is facing.

e.g.
`return ["attack"]`

:::tip

In most game modes, there is a speed penalty when your character is attacking. (i.e. your character slows down while attacking and moving at the same time)

:::

### shield

| <small>**script**:`shield` **manual**:`s`</small>

Your character can defend itself by raising a shield. While the shield is up, your character will recieve no damage

e.g.
`return ["shield"]`

:::info
Shields have a short lifespan. They break when hit or when they run out of energy.
:::

:::tip
Shields have a cooldown so use them wisely
:::

### dash

| <small>**script**:`dash`, **manual**:`d`</small>

Dash will temporarily increase your player's speed in whatever direction they are moving.

Dash is a combat mechanic. It is only enabled if there are enemies within 300 radius of the player.

There is a `1s` cooldown on this ability.

:::tip
Use this to surprise attack an enemy, or escape an attack.
:::

### special

| <small>**script**:`special` **manual**:`f`</small>

Use whichever special attack is equipped on the player. See [Power Ups](/docs/game-play/power-ups) section below for details on available special attacks (Bomb, Freeze, Shockwave).

e.g.
`return ["special"]`

:::tip
Specials have a cooldown so use them wisely
:::

:::info
You won't lose a power up after you're killed. It seems more fun that way (for now?)
:::

## Actions

In addition to movement, a character can take actions.

### Use Items

| <small>**script**:`{"use": "<item>"}` **manual**:`x(big_potion)/c(speed_zapper)/v(ring)`</small>

There are three items availale for use in the game - `big_potion`s, `ring`s and `speed_zapper`s. Once you collect the items, you can use them.

To use them, return a `use` action with the specified item.

e.g.
`return [{"use": "ring"}]`

:::info
Big Potions - replenish your health

Speed Zappers - a weapon you can fire that will slow down anything in it's blast radius
:::

Rings - cloaks your player to hide from enemies and other players

### Speak

| <small>**script**:`{"speak": "Hello there!}` **manual**:`not supported`</small>

Your character can speak. Returning the speak action will display the message next to your character for all to see.

e.g. `return [{"speak": "Hello there"}]`

### Redeeming Skill Points

| <small>**script**:`{"redeem_skill_point": "<skill_type>"}` **manual**:`e(attack)/w(speed)/q(health)`</small>

As you gain `xp`, your character levels up. Each level (up to level 20) will come with `skill points` you can redeem to boost your characters abilities.

You can apply skill points to `health`, `speed`, or `attack`.

e.g.
`return [{"redeem_skill_point": "attack"}]`

:::tip
Come up with a strategy to build up your characters skill. Speed allows you to collect items and escape attacks while health and attack may give you the upper hand in battle.
:::

:::info
Skill points are rewarded for levelling up until you reach Level 20. Beyond that you no longer receive additional skill points.
:::

## Debugging

| <small>**script**:`debug_info` **manual**:`not supported`</small>

You can send some information to the debug panel in game. Return a "debug_info" object in your api response array

```
	"debug_info": {
		"target_id": <id of the target object>,
		"message": <150 char limit>,
	}
```
