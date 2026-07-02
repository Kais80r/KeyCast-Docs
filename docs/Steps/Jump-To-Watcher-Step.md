# Jump to Watcher Step

Jump to Watcher Step jumps to a numbered step inside the current watcher.

## Fields

| Field | Meaning |
| --- | --- |
| Step number | The watcher step to continue from |

## Where It Works

This step only works inside a watcher.

## Setup From Scratch

1. Create a watcher.
2. Add multiple watcher steps.
3. Add Jump to Watcher Step.
4. Enter the watcher step number.
5. Test carefully to avoid endless loops.

## Example

```text
Watcher steps:
1. Status Message Checking again
2. Wait 1 second
3. Jump to Watcher Step 1
```

## Useful For

- Loops inside a watcher.
- Rechecking a recovery state.
- Repeating watcher-only actions.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The step does nothing useful outside a watcher | Use it only inside watcher steps |
| The watcher loops forever | Add a clear exit such as Stop Sequence, Reset and Restart Sequence, or Jump Sequence Step |
| The jump target is wrong | Use watcher step numbers, not main sequence step numbers |
