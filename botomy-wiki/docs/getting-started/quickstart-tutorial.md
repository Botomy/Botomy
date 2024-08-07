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

## Collect a coin

1. Get the location of a coin

```python
func play(level_data):
# highlight-start
	# get the first coin in the array
	var coin = level_data.coins[0]

	# print the x,y coordinates of the coin
	print(coin.position)
# highlight-end
	return []
```

2. Get your character's position

```python
func play(level_data):
# highlight-start
	# get the first coin in the array
	var coin = level_data.coins[0]

	# print the x,y coordinates of the coin
	debug(coin.position)

	# highlight-start
	var own_player = level_data.own_player
	debug(own_player.position)
	# highlight-end
	return []
```

3. Determine what direction the coin is relative to your character

```python
func play(level_data):
	# get the first coin in the array
	var coin = level_data.coins[0]

	# print the x,y coordinates of the coin
	debug(coin.position)

	var own_player = level_data.own_player
	debug(own_player.position)

	# highlight-start
	if own_player.position.x > coin.position.x:
  	debug("coin is left of character")
	else:
  	debug("coin is right of character")

	if own_player.position.y > coin.position.y:
  	debug("coin is above character")
	else:
		debug("coin is below character")
	# highlight-end
	return []
```

4. Return the moves to get to the coin

```python
func play(level_data):
	# get the first coin in the array
	var coin = level_data.coins[0]

	# print the x,y coordinates of the coin
	debug(coin.position)

	var own_player = level_data.own_player
	print(own_player.position)

	# highlight-start
	var moves = []
	if own_player.position.x > coin.position.x:
		debug("coin is left of character")
		moves.append("move_left")
	else:
		debug("coin is right of character")
		moves.append("move_right")

	if own_player.position.y > coin.position.y:
		debug("coin is above character")
		moves.append("move_up")
	else:
		debug("coin is below character")
		moves.append("move_down")

	debug(moves)

	# highlight-end
	return []
```

5. Go pick up the coin!

```python
func play(level_data):
	# get the first coin in the array
	var coin = level_data.coins[0]

	# print the x,y coordinates of the coin
	debug(coin.position)

	var own_player = level_data.own_player
	print(own_player.position)


	var moves = []
	if own_player.position.x > coin.position.x:
		debug("coin is left of character")
		moves.append("move_left")
	else:
		debug("coin is right of character")
		moves.append("move_right")

	if own_player.position.y > coin.position.y:
		debug("coin is above character")
		moves.append("move_up")
	else:
		debug("coin is below character")
		moves.append("move_down")

	debug(moves)

	# highlight-start
	return moves
	# highlight-end
```

### Congratulations

Your character is now able to move towards a coin. Go forth and implement more functionality. Conquer more worlds!

:::tip
Is your character bobbing up and down and back and forth? Try modifying the code to detect if the character is in line with the coin already. This may require you to have a margin of error (i.e. sometimes it's better to say 11 ~= 10)
:::
