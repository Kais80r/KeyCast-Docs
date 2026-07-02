# Choosing What To Use

Use the simplest item type that fits the job.

The right choice depends on what the automation needs to understand. A track only replays actions. A sequence can make decisions.

## Quick Decision Table

| Question | Best choice |
| --- | --- |
| Do you only need to replay input? | Track |
| Do you need a reusable editable action list? | Advanced Track |
| Do you need values, If steps, Read Text, loops, or watchers? | Sequence |
| Do you need recovery logic while work is running? | Sequence with watchers |

## Decision Flow

Start at the top and stop when a line matches.

| If this is true | Use this |
| --- | --- |
| The action is always the same and the screen is already ready | [Track](Track.md) |
| The action is a reusable block and watcher logic can stay in the calling sequence | [Advanced Track](Advanced-Track.md) |
| The workflow needs to wait, check, read, count, branch, message, or recover | [Sequence](Sequence.md) |
| Something can happen at an unexpected time | [Sequence](Sequence.md) with [Watchers](../Watchers/README.md) |

## Choose Track When

- The action is short.
- The UI position is stable.
- There is no decision to make.
- The workflow uses fixed input without screen text reading.
- You can replay the same input every time.

Example:

```text
Record a short action, save it as a track, and press Play.
```

Good track examples:

- Press one shortcut.
- Click through a small stable menu.
- Fill a small fixed form section.
- Repeat a short action that starts from the same screen state.

Avoid a plain track when:

- The target moves.
- The app may not be ready.
- Text or images decide what should happen next.
- A popup or error might appear.

## Choose Advanced Track When

- The action is more than a simple recording.
- You want to edit the steps.
- You want to reuse the same action block in multiple places.
- Watchers can live in the sequence that runs this item.

Example:

```text
Create an advanced track named Prepare Report.
Use it from several sequences with Run Advanced Track.
```

Good advanced track examples:

- Open the same tool and arrange the window.
- Fill a reusable form section.
- Run cleanup steps used by multiple sequences.
- Create a reusable setup block before the main workflow.

Avoid putting the whole workflow into an advanced track if it needs values, watchers, or complex recovery.

## Choose Sequence When

- The workflow needs decisions.
- The screen can change.
- You need to read text into a value.
- You need loops or retry limits.
- You need watchers.
- You need messages with live values.

Example:

```text
1. Run Advanced Track Prepare Report
2. Read Text statusText
3. If Sequence Value statusText contains Complete
4. Send message or continue
```

Good sequence examples:

- Wait until visible text appears before clicking.
- Read a status label and send it in a message.
- Repeat steps until a value reaches a limit.
- Stop or recover when an error appears.
- Use a watcher to react while the normal path keeps running.

## Common Wrong Choices

| Problem | Better choice |
| --- | --- |
| A track clicks the wrong place because the app was not ready | Sequence with Wait For (Text) or Wait For (Window) |
| An advanced track needs background recovery checks | Put it inside a sequence and add watchers |
| A sequence is huge because the same block repeats everywhere | Move that block into an advanced track |
| A watcher handles the normal expected path | Put that logic into main steps instead |

## Common Pattern

Use all three together:

```text
Track:
Small recorded input

Advanced Track:
Reusable action block

Sequence:
Main workflow that runs tracks, reads values, branches, loops, and watches for problems
```

This keeps each piece easier to understand and fix.

## Next Pages

- [Track](Track.md)
- [Advanced Track](Advanced-Track.md)
- [Sequence](Sequence.md)
- [Getting Started](../Getting-Started.md)
