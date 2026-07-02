# Using Status Messages While Building

Status Message is one of the best steps for testing.

It shows what the sequence is doing without needing Discord, files, or other external systems.

## What To Put In A Status Message

You can use plain text:

```text
Reached the wait step
```

You can also include values:

```text
Current state: {statusText}
Loop count: {Loops}
Read text: {readText}
```

## Where To Put Them

Useful places:

- Before an If step.
- Inside the Then path.
- Inside the Else path.
- At the start of a watcher.
- After Read Text.
- After Change Sequence Value.

## When To Remove Them

Keep messages that are useful during normal use.

Remove messages that were only used to find a bug, especially if they make the status area noisy.

## Status Before Discord

If a Discord Message does not work, test the same text with Status Message first.

If the Status Message looks correct, the value replacement works and the problem is probably the Discord setup.
