# Wait

Wait pauses the current step list for a fixed number of seconds.

## Fields

| Field | Meaning |
| --- | --- |
| seconds | How long to wait |

## Setup From Scratch

1. Add Wait after an action.
2. Enter the number of seconds.
3. Keep it as short as the workflow safely allows.
4. Replace it with a Wait for step if there is a real screen state to wait for.

## Example

```text
1. Click Text Refresh
2. Wait 1.5 seconds
3. Wait For (Text) Ready timeout 30
```

## Useful For

- Small pauses after clicks.
- Giving menus time to open.
- Giving windows time to focus.
- Making recorded input more stable.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Fixed waits are unreliable | Use [Wait For (Text)](Wait-For.md), [Wait For (Image)](Wait-For.md), or [Wait For (Window)](Wait-For.md) for real readiness checks |
| The sequence feels slow | Replace unnecessary fixed waits with condition-based waits |
| A watcher fires during the wait | Check whether the watcher should pause, stop, or ignore that condition |
