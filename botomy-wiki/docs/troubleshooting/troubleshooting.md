# Troubleshooting

## API Errors

Check for the following:

### Invalid return values

Your function **must** return an _array_. The array must be empty, or be filled with valid character moves/actions.

Things that are not valid returns:

- `null`, `undefined` or otherwise `empty` values (other than an empty array)

## Windows

### API Loop is slow

If API calls are painfully slow and lagging on Windows, check that you're not using `localhost`. Switch to `127.0.0.1`.
