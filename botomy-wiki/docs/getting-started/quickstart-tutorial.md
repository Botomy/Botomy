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
	print_message(item.position)
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
	print_message(item.position)

	# highlight-start
	var own_player = level_data.own_player
	print_message(own_player.position)
	# highlight-end
	return []
```

4. Build the command to move towards the item

```python
func play(level_data):
	# get the first item in the array
	var item = level_data.items[0]

	# print the x,y coordinates of the item
	print_message(item.position)

	var own_player = level_data.own_player
	print_message(own_player.position)

	# highlight-start
	var moves = []
	moves.append({"move_to": item.position})
	print_message(moves)

	# highlight-end
	return []
```

5. Go pick up the item!

```python
func play(level_data):
	# get the first item in the array
	var item = level_data.items[0]

	# print the x,y coordinates of the item
	print_message(item.position)

	var own_player = level_data.own_player
	print_message(own_player.position)


	var moves = []
	moves.append({"move_to": item.position})
	print_message(moves)

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

## Starter Bot

Here's a basic functional to start hacking!

```
func get_closest_item(position, items):
	var min_dist = INF
	var target = null
	for item in items:
		var dist = dist_squared_to(position, item.position)
		if dist < min_dist:
			min_dist = dist
			target = item
	return target

func dist_squared_to(a, b):
	return pow(a.x - b.x,2) + pow(a.y-b.y,2)

func play(level_data):
	var moves = []
	var own_player = level_data.own_player
	var items = level_data.items
	var enemies = level_data.enemies

	var potential_targets = []

	# check if we have room to collect more big_potions otherwise ignore items
	if own_player.items.big_potions.size() < 6:
		potential_targets.append_array(items)

	potential_targets.append_array(enemies)

	var target = get_closest_item(own_player.position, potential_targets)

	if not target == null:
		moves.append({"move_to": target.position})

		# if the target has health then it's probably something that should be killed
		if target.has("health") and target.health > 0 and dist_squared_to(own_player.position, target.position) < 15625:
			moves.append("attack")
			moves.append({"use":"speed_zapper"})
			moves.append("shield")

	if own_player.health < own_player.max_health:
		moves.append({"use": "big_potion"})

	if own_player.levelling.available_skill_points > 0:
		moves.append({"redeem_skill_point": "health"})

	return moves
```
