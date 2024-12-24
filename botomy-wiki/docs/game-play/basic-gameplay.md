---
sidebar_position: 1
---

# Basic Gameplay

## Play modes

To enable a play mode, select the tab and press **RUN**. You can stop execution at any time by pressing **STOP**.

:::info
You can only run one mode at a time. Pressing **RUN** in one mode will stop execution in another mode.
:::

There are three supported play modes (see below):

### ScriptEditor

The language used in **script** mode is [GDScript](https://docs.godotengine.org/en/4.2/tutorials/scripting/gdscript/gdscript_basics.html).

Your script must define a `play` function that takes a single argument (`level_data`).

:::info

The `play(level_data)` function is called by the game engine (_mostly_) on every frame .

:::

The function should return the list of moves (i.e. key presses) that the bot should follow.

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

## Movement

| <small>**script**:`move_to` **manual**:`arrow keys`</small>

Your player will move to a given x,y target.
`move_to: {x, y}`

e.g.
`return [{"move_to": {"x": 10, "y": 20}}]`

:::info

Your player will navigate to the target using basic astar pathfinding (built into the engine)

:::

## Dash

| <small>**script**:`dash`, **manual**:`d`</small>

Dash will temporarily increase your player's speed in whatever direction they are moving.

There is a `1s` cooldown on this ability.

## Actions

In addition to movement, a character can take actions.

### Attack

| <small>**script**:`attack` **manual**:`space bar`</small>

This will cause the character to attack in the direction it is facing.

e.g.
`return ["attack"]`

:::tip

In most game modes, there is a speed penalty when your character is attacking. (i.e. your character slows down while attacking and moving at the same time)

:::

### Raise Shield

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

### Speak

| <small>**script**:`{"speak": "Hello there!}` **manual**:`not supported`</small>

Your character can speak. Returning the speak action will display the message next to your character for all to see.

e.g. `return [{"speak": "Hello there"}]`

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

### Redeeming Skill Points

| <small>**script**:`{"redeem_skill_point": "<skill_type>"}` **manual**:`e(attack)/w(speed)/q(health)`</small>

In some maps (i.e. Fight World), you can gain `xp` and level up. Each level will come with `skill points` you can redeem to boost your characters abilities.

You can apply skill points to `health`, `speed`, or `attack`.

e.g.
`return [{"redeem_skill_point": "attack"}]`

:::tip
Come up with a strategy to build up your characters skill. Speed allows you to collect items and escape attacks while health and attack may give you the upper hand in battle.
:::

### Special Attack

| <small>**script**:`special` **manual**:`f`</small>

Use whichever special attack is equipped on the player

e.g.
`return ["special"]`

:::tip
Specials have a cooldown so use them wisely
:::

:::info
You won't lose a power up after you're killed. It seems more fun that way (for now?)
:::

#### Bomb

```
	"max_damage": 200,
	"damage_factor": 2.5, // factor of the player's current attack damage
	"cooldown": 1.5,
```

:::warn
Bombs can do self damage. Be careful after you've dropped a bomb.
:::

#### Freeze

```
	"cooldown": 1.5,
	"duration": 1.0, // how long an enemy will be frozen for (sec)
	"max_damage": 20,
	"damage_factor": 0.33, // factor of the player's current attack damage
	"damage_absorption_factor": 0.3, // how much damage is asborbed by the ice when frozen (i.e. when frozen, damage is received at 70%)
```

#### Shockwave

```
	"duration": 0.2,
	"cooldown": 1.5,
	"speed": 1500,
	"max_damage": 15,
	"damage_factor": 0.2, // factor of the player's current attack damage
```

## Kill Streaks

If your player gets high enough kill streaks, it will begin overclocking. Overclocking lasts for 15s.
Each additional kill will reset the 15s timer.

### Speed

```
	"streak": 50,
	"value": 1.3, # overclocked speed is 1.3 times the base speed
```

### Damage

```
	"streak": 100,
	"value": 1.2, # overclocked damage is 1.2 times the base damage
```

### Health Regen

```
	"streak": 150,
	"value": 10, # overclocked health regen points per second
```

## Debugging

There is a single function to print messages to the console - `print_message(msg)`
:::tip
`print_message(level_data)` to see what information your function gets every frame. This will help you decide what moves to return
:::

:::warning
Any script level error (e.g. syntax) will not be displayed. You will only see a `script error message` (good luck!)
:::
