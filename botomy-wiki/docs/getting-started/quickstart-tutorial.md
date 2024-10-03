---
sidebar_position: 2
---

# Quickstart Tutorial

## Start a game

Go into the **Offline Practice** mode and select the "Tutorial" map.

Press "Start"

## Use the script play mode

Select the `ScriptEditor` tab (probably already selected).

Press "Run" to start executing the default script. You should see your character say "hello there"

## Collect an item

1. Get the location of an item

```python
func play(level_data):
# highlight-start
	# get the first item in the array
	var item = level_data.items[0]

	# print the x,y coordinates of the item
	print(item.position)
# highlight-end
	return []
```

2. Get your character's position

```python
func play(level_data):
# highlight-start
	# get the first item in the array
	var item = level_data.items[0]

	# print the x,y coordinates of the item
	debug(item.position)

	# highlight-start
	var own_player = level_data.own_player
	debug(own_player.position)
	# highlight-end
	return []
```

4. Build the command to move towards the item

```python
func play(level_data):
	# get the first item in the array
	var item = level_data.items[0]

	# print the x,y coordinates of the item
	debug(item.position)

	var own_player = level_data.own_player
	print(own_player.position)

	# highlight-start
	var moves = []
	moves.append({"move_to": item.position})
	debug(moves)

	# highlight-end
	return []
```

5. Go pick up the item!

```python
func play(level_data):
	# get the first item in the array
	var item = level_data.items[0]

	# print the x,y coordinates of the item
	debug(item.position)

	var own_player = level_data.own_player
	print(own_player.position)


	var moves = []
	moves.append({"move_to": item.position})
	debug(moves)

	# highlight-start
	return moves
	# highlight-end
```

### Congratulations

Your character is now able to move towards an item. Go forth and implement more functionality. Conquer more worlds!

:::tip

In GDScript there are some handy functions

| To compare floats, use the is_equal_approx() and is_zero_approx() functions instead.

https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/gdscript_basics.html#operators
:::
