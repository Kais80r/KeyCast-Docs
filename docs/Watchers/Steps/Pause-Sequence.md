# Pause Sequence

Pause Sequence is a watcher step that tells the main sequence to stop where it is and let the watcher take over.

## Without Pause Sequence

The watcher runs beside the main sequence.

Example:

```text
Watcher steps:
1. Status Message Text appeared
```

The main sequence keeps going.

## With Pause Sequence

The watcher takes control.

Example:

```text
Watcher steps:
1. Pause Sequence
2. Click Text OK
3. Jump Sequence Step 5
```

The main sequence pauses, the watcher handles the situation, then Jump Sequence Step decides where the sequence continues.

## Why The Position Matters

If Pause Sequence is after other watcher steps, those earlier steps can run while the main sequence is still running.

Example:

```text
Watcher steps:
1. Press key Escape
2. Pause Sequence
3. Jump Sequence Step 2
```

This can be intentional, but it can also cause confusing behavior. If the watcher should take over immediately, put Pause Sequence first.

## How To Continue

After Pause Sequence, choose one of these:

| Step | Result |
| --- | --- |
| Jump Sequence Step | Continue from a specific main step |
| Reset and Restart Sequence | Reset values to Starting Values and start the sequence again |
| Stop Sequence | End the sequence |

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The sequence stays paused | Add Jump Sequence Step, Reset and Restart Sequence, or Stop Sequence after recovery |
| Main steps keep running too long | Put Pause Sequence before watcher steps that click, type, jump, or change values |
| The watcher fires again immediately | Increase the cooldown or make the trigger more specific |

## More About

- [Pause Sequence step](../../Steps/Pause-Sequence.md)
- [Jump Sequence Step](../../Steps/Jump-Sequence-Step.md)
- [Watcher Recovery Workflow](../../Guides/Watcher-Recovery-Workflow.md)
