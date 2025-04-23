# Troubleshooting

## Script errors

Check for the following:

### Invalid return values

Your function **must** return an _array_. The array must be empty, or be filled with valid character moves/actions.

Things that are not valid returns:

- `null`, `undefined` or otherwise `empty` values (other than an empty array)
