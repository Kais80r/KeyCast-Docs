# What Is A Trigger

A trigger is the "when" part of a watcher.

Example:

```text
When Text Complete is seen
```

This means:

```text
If WhirlyTask sees the text Complete, run the watcher steps.
```

## Trigger Versus Watcher Steps

The trigger only decides if the watcher should start.

The watcher steps decide what happens after it starts.

Example:

```text
Trigger:
When Text Error is seen

Watcher steps:
1. Pause Sequence
2. Click Text OK
3. Jump Sequence Step 4
```

## Why A Trigger May Not Fire

Common reasons:

- The sequence is not currently running.
- The watcher is off.
- The selected area does not include the thing being checked.
- The condition is too strict.
- The cooldown is still active.
- The value or text is not exactly what you think it is.

Use a Status Message step in the watcher while testing. That tells you whether the trigger fired at all.

## More About

- [Watcher Triggers](README.md)
- [Watchers](../README.md)
- [Watcher Does Not Fire](../../Troubleshooting/Watcher-Does-Not-Fire.md)
