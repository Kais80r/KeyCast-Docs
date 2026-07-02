# Sequence

A sequence is a full workflow.

Use a sequence when the automation needs steps, decisions, values, screen reading, loops, or watchers.

A sequence is the best choice when the app may be in different states and WhirlyTask needs to react.

## What A Sequence Contains

| Part | Meaning |
| --- | --- |
| Starting Values | Values that exist when the sequence starts |
| Main Steps | The normal path of the workflow |
| Watchers | Background checks that can react while the sequence runs |

## How To Think About It

The main steps should describe the normal expected path.

Watchers should describe side events:

```text
Main steps:
Do the normal workflow

Watcher:
If an unexpected warning appears, pause and handle it
```

Values connect steps together:

```text
Read Text fills resultText
If Sequence Value checks resultText
Discord Message sends {resultText}
```

## What A Sequence Is Good For

Sequences are best for workflows that need logic.

Examples:

```text
Wait until text appears
Read visible text into a value
Click a button by text
Retry until success
Stop after too many attempts
React to popups
Send status or Discord messages
Use a saved track as one part of a larger workflow
```

## Setup From Scratch

1. Add starting values you already know you need.
2. Build the first few main steps.
3. Add [Status Message](../Steps/Status-Message.md) steps while testing.
4. Run the sequence.
5. Add loops, branches, or values after the simple path works.
6. Add watchers only for events that can happen outside the normal path.
7. Press Save before closing the editor.

## Sequence Example

```text
Starting Values:
statusText starts as empty
attempts starts as 0

Main Steps:
1. Change Sequence Value attempts Add 1
2. Read Text statusText from selected status area
3. If Sequence Value statusText contains Complete
   Then:
   1. Status Message Finished
   2. Stop Sequence
   Else:
   1. Wait 2 seconds
   2. Jump Sequence Step 1
```

## Watcher Example

```text
Watcher trigger:
When Text Warning is seen

Watcher steps:
1. Pause Sequence
2. Click Text OK
3. Jump Sequence Step 2
```

This watcher pauses the main sequence before recovery. Without Pause Sequence, the watcher steps can run while the main steps keep moving.

## When To Use A Sequence

Use a sequence when you need:

- Screen text reading.
- Image or text conditions.
- Values.
- Branches.
- Loops.
- Watchers.
- Recovery logic.
- Messages with live values.

## Common Sequence Patterns

| Pattern | Use it when | Open |
| --- | --- | --- |
| Basic loop | Steps should repeat | [Basic Loop](../Examples/Basic-Loop.md) |
| Counter limit | A loop should stop after a maximum count | [Counter Limit](../Examples/Counter-Limit.md) |
| Read and decide | Screen text controls the next step | [Read Text](../Steps/Read-Text.md) |
| Watcher recovery | Unexpected errors should be handled | [Watcher Recovery](../Examples/Watcher-Recovery.md) |
| Notification system | WhirlyTask should report progress or results | [Notification System](../Examples/Notification-System.md) |

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Changes disappear | Press Save before closing the editor or testing from the main window |
| Values reset unexpectedly | Check whether [Reset and Restart Sequence](../Steps/Reset-And-Restart-Sequence.md) runs before the value is used |
| Text or image detection fails | Select a slightly larger area with margin around the target |
| A watcher runs but the main sequence keeps moving | Put [Pause Sequence](../Steps/Pause-Sequence.md) near the start of the watcher |
| The sequence is hard to follow | Move repeated action blocks into tracks or advanced tracks |
| Watchers handle normal expected steps | Move the normal path into main steps and save watchers for unexpected events |

Useful examples: [Basic Loop](../Examples/Basic-Loop.md), [Watcher Recovery](../Examples/Watcher-Recovery.md), [Counter Limit](../Examples/Counter-Limit.md), [Notification System](../Examples/Notification-System.md)

## More About

- [Steps](../Steps/README.md)
- [Values](../Values/README.md)
- [Watchers](../Watchers/README.md)
- [Troubleshooting](../Troubleshooting/README.md)
