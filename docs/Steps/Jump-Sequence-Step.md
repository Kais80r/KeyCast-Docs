# Jump Sequence Step

Jump Sequence Step jumps to a numbered step in the main sequence.

## Fields

| Field | Meaning |
| --- | --- |
| Step number | The main sequence step to continue from |

## Setup From Scratch

1. Find the main step number that should run next.
2. Add Jump Sequence Step.
3. Enter that number.
4. Test after any edit that changes step order.

## Example: Continue After Watcher Recovery

```text
Watcher steps:
1. Pause Sequence
2. Click Text OK
3. Jump Sequence Step 4
```

## Example: Main Loop

```text
1. Do work
2. Wait 1 second
3. Jump Sequence Step 1
```

## Useful For

- Continuing after Pause Sequence.
- Main sequence loops.
- Returning to a known point after recovery.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The jump target is wrong | Recheck the main sequence step number after editing steps |
| Values should be kept | Use Jump Sequence Step instead of [Reset and Restart Sequence](Reset-And-Restart-Sequence.md) |
| A watcher needs to return to the main flow | Use Jump Sequence Step, not Jump Block Step |
