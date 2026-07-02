# Watcher Pauses And Never Continues

This page is for watchers that pause the main sequence and then leave it stuck.

## Why It Happens

Pause Sequence stops the main sequence. After that, the watcher must decide what happens next.

## Fix

After Pause Sequence, add one of these:

| Step | Use when |
| --- | --- |
| Jump Sequence Step | Continue at a specific main step |
| Reset and Restart Sequence | Reset values to Starting Values and start the workflow again |
| Stop Sequence | End the workflow |

## Example

```text
Watcher steps:
1. Pause Sequence
2. Click Text OK
3. Jump Sequence Step 4
```

## More About

- Pause Sequence: [Pause Sequence](../Watchers/Steps/Pause-Sequence.md)
- Watcher recovery example: [Watcher Recovery](../Examples/Watcher-Recovery.md)
- Jump Sequence Step: [Jump Sequence Step](../Steps/Jump-Sequence-Step.md)
- Reset and Restart Sequence: [Reset and Restart Sequence](../Steps/Reset-And-Restart-Sequence.md)
- Stop Sequence: [Stop Sequence](../Steps/Stop-Sequence.md)
