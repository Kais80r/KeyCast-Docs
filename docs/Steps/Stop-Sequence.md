# Stop Sequence

Stop Sequence ends the current playback.

## Fields

This step has no fields.

## Setup From Scratch

1. Add Stop Sequence where playback should end.
2. If it is inside a branch, make sure the other branch also has the correct next action.
3. Use Status Message before it while testing.

## Example

```text
If Sequence Value attempts >= 3
Then:
1. Status Message Too many attempts
2. Stop Sequence
```

## Useful For

- Ending successful workflows.
- Stopping after too many retries.
- Stopping after a watcher detects a serious problem.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The sequence should start over | Use [Reset and Restart Sequence](Reset-And-Restart-Sequence.md) instead |
| A branch stops too early | Move Stop Sequence only into branches where playback should end |
| Later steps do not run | Remember that Stop Sequence ends playback immediately |
