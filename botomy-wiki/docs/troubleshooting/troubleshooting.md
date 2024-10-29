# Troubleshooting

:::warning
If you're using the web version you're on your own. Just install the desktop apps - thank me later.
:::

## Can't open the Mac app

I don't have a developer license from Apple yet so I can't sign the build.

To open, right-click and press open from the menu.

For newer MacOS versions, you must go to Privacy & Security settings to allow the app to open (after you tried opening it)

Yes - I'll get a developer license soon.

## Script errors

Check for the following:

### Invalid return values

Your function **must** return an _array_. The array must be empty, or be filled with valid character moves/actions.

Things that are not valid returns:

- `null`, `undefined` or otherwise `empty` values (other than an empty array)

### Invalid script syntax

GDScript is whitespace sensitive. Paste your code into a gdscript editor to check for any syntax errors.

Here are some of their [recommended editors](https://gdscript.com/articles/godot-code-editors/)

or

Try this online editor here https://gd.tumeo.space/
