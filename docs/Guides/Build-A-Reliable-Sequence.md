# Build A Reliable Sequence

This guide explains a practical way to build a sequence without making it confusing too quickly.

A reliable sequence is not just a long list of actions. It has a clear normal path, visible test points, values with good names, and watchers only where they are useful.

## 1. Describe The Normal Path

Write the normal path first.

Example:

```text
1. Focus the target window
2. Run setup actions
3. Wait until the screen is ready
4. Read or check the result
5. Send a message or continue
```

Add watchers after the normal path works. They are easier to design once the expected flow is clear.

## 2. Add Only The First Few Steps

Start with a small version:

```text
1. Focus Window
2. Wait For (Text) Ready
3. Status Message Ready reached
4. Stop Sequence
```

Run it. If this part is unreliable, fix it before adding more logic.

## 3. Add Status Messages While Testing

Status messages are temporary signs inside WhirlyTask.

Useful testing messages:

```text
Starting setup
Ready text found
Read value: {resultText}
Attempt: {attempts}
Entering recovery watcher
```

When the sequence is stable, you can remove messages that are only useful for debugging.

## 4. Add Values When Steps Need To Share Information

Use a value when one step creates information and another step needs it.

Common values:

```text
statusText starts as empty
resultText starts as empty
attempts starts as 0
state starts as waiting
```

Examples:

| Need | Value pattern |
| --- | --- |
| Read text and decide | `Read Text resultText`, then `If Sequence Value resultText contains Complete` |
| Count loops | `Change Sequence Value attempts Add 1` |
| Send a live message | `Discord Message Result: {resultText}` |
| Let a watcher react | `When Sequence Value state changed` |

More detail: [Values](../Values/README.md)

## 5. Add Loops Carefully

A loop usually means a step jumps back to an earlier step.

Basic loop:

```text
1. Do work
2. Wait 5 seconds
3. Jump Sequence Step 1
```

Safer loop with a counter:

```text
Starting Values:
loops starts as 0

Main Steps:
1. Change Sequence Value loops Add 1
2. Do work
3. Wait 5 seconds
4. Jump Sequence Step 1

Watcher:
When Sequence Value loops >= 30
1. Stop Sequence
```

More detail: [Counter Limit](../Examples/Counter-Limit.md)

## 6. Add Watchers For Side Events

Use watchers for events that can happen at unexpected times.

Good watcher jobs:

- Stop when a dangerous state appears.
- Pause and recover when an error appears.
- Send an alert when something important appears.
- Refocus a window if the workflow loses focus.

Avoid using watchers for the normal path. If the sequence is always waiting for a known text before the next step, use [Wait For (Text)](../Steps/Wait-For.md) in the main steps.

## 7. Decide How Watchers Continue

Every watcher that pauses the sequence should clearly continue, reset, or stop.

| Desired result | End with |
| --- | --- |
| Continue at a known main step | [Jump Sequence Step](../Steps/Jump-Sequence-Step.md) |
| Start over and reset values | [Reset and Restart Sequence](../Steps/Reset-And-Restart-Sequence.md) |
| End playback | [Stop Sequence](../Steps/Stop-Sequence.md) |

If the watcher only sends a notification, it may not need Pause Sequence.

## 8. Save And Test Again

After a group of changes:

1. Press Save.
2. Run from the beginning.
3. Watch the status text.
4. Confirm values are changing the way you expect.
5. Test one failure case if the sequence has watchers.

## Common Build Problems

| Problem | Likely fix |
| --- | --- |
| It works once, then fails later | Add waits or focus steps before the unreliable action |
| A value is blank | Make sure a step fills it before it is used |
| A watcher fires too often | Increase cooldown or make the trigger more specific |
| A watcher pauses forever | Add Jump Sequence Step, Reset and Restart Sequence, or Stop Sequence |
| Read Text is wrong | Make the selected area larger and test with Status Message |

## More About

- [Getting Started](../Getting-Started.md)
- [Steps](../Steps/README.md)
- [Watchers](../Watchers/README.md)
- [Testing A Sequence](../Tips/Testing-A-Sequence.md)
- [Troubleshooting](../Troubleshooting/README.md)
