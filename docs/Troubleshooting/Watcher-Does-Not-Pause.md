# Watcher Does Not Pause

This page is for watchers that fire but the main sequence keeps running.

## Main Rule

Watchers run alongside the main sequence by default.

It only pauses the main sequence when it reaches a Pause Sequence step.

## Fix

Add Pause Sequence inside the watcher.

If the watcher should take over immediately, make Pause Sequence the first watcher step.

Example:

```text
Watcher steps:
1. Pause Sequence
2. Handle the problem
3. Jump Sequence Step 4
```

## If Pause Sequence Is Not First

Steps before Pause Sequence can run while the main sequence is still running. This can be useful, but it can also be confusing.

## More About

- Pause Sequence: [Pause Sequence](../Watchers/Steps/Pause-Sequence.md)
- Watchers: [Watchers](../Watchers/README.md)
- Watcher recovery example: [Watcher Recovery](../Examples/Watcher-Recovery.md)
- Watcher tips: [Keeping Watchers Predictable](../Tips/Keeping-Watchers-Predictable.md)
