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

| <small>**script**:`move_left`,`move_right`,`move_up`,`move_down`, **manual**:`arrow keys`</small>

There are four different directions your character can move in - left, right, up, and down.

`move_left`
`move_right`
`move_up`
`move_down`

e.g.
`return ["move_left"]`

:::info

If you want the character to move diagonnally up and right, then `return ["move_up", "move_right"]`.

:::

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

| <small>**script**:`raise_shield` **manual**:`s`</small>

Your character can defend itself by raising a shield. While the shield is up, your character will recieve no damage

e.g.
`return ["raise_shield"]`

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

| <small>**script**:`{"use": "<item>"}` **manual**:`z(feather)/x(big_potion)`</small>

There are two items availale for use in the game - `big_potion`s and `feather`s. Once you collect the items, you can use them.

To use them, return a `use` action with the specified item.

e.g.
`return [{"use": "feather"}]`

:::info
Feathers - increase your movement speed

Big Potions - replenish your health
:::

:::tip
Speed boosts can stack. Try collecting a few feathers and use multiple in a row for maximum speed boost.
:::

### Redeeming Skill Points

| <small>**script**:`{"redeem_skill_point": "<skill_type>"}` **manual**:`c(attack)/v(speed)/b(health)`</small>

In some maps (i.e. Fight World), you can gain `xp` and level up. Each level will come with `skill points` you can redeem to boost your characters abilities.

You can apply skill points to `health`, `speed`, or `attack`.

e.g.
`return [{"redeem_skill_point": "attack"}]`

:::tip
Come up with a strategy to build up your characters skill. Speed allows you to collect items and escape attacks while health and attack may give you the upper hand in battle.
:::

## Debugging

There is a single function to print messages to the console - `debug(msg)`
:::tip
`debug(level_data)` to see what information your function gets every frame. This will help you decide what moves to return
:::

:::warning
Any script level error (e.g. syntax) will not be displayed. You will only see a `script error message` (good luck!)
:::
