# Pause Sequence

Pause Sequence lets a watcher take control from the main sequence.

## Where It Works

Pause Sequence is meant for watcher steps. If it is used outside a watcher, WhirlyTask reports that it only works inside a watcher.

## Fields

This step has no fields.

## Setup From Scratch

1. Create a watcher.
2. Choose the trigger.
3. Add Pause Sequence as the first watcher step if the watcher should take over immediately.
4. Add recovery steps.
5. End with Jump Sequence Step, Reset and Restart Sequence, or Stop Sequence.

## Example

```text
Watcher steps:
1. Pause Sequence
2. Click Text OK
3. Jump Sequence Step 4
```

## Why Position Matters

Steps before Pause Sequence can run while the main sequence is still running.

If the watcher should stop the main path first, put Pause Sequence first.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The sequence stays paused | End the watcher with Jump Sequence Step, Reset and Restart Sequence, or Stop Sequence |
| Recovery starts too late | Put Pause Sequence before recovery clicks, keys, jumps, or value changes |
| The step reports that it only works in a watcher | Use Pause Sequence only inside watcher steps |

More detail: [Watcher Pause Sequence](../Watchers/Steps/Pause-Sequence.md)

## More About

- Full recovery workflow: [Watcher Recovery Workflow](../Guides/Watcher-Recovery-Workflow.md)
- Watchers: [Watchers](../Watchers/README.md)
- Watcher pauses and never continues: [Watcher Pauses And Never Continues](../Troubleshooting/Watcher-Pauses-And-Never-Continues.md)
