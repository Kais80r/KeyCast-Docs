# Advanced Track

An advanced track is an editable list of steps that can be reused.

It is more structured than a simple recorded track, but it is still not the same as a full sequence.

Use an advanced track when you want a reusable action block, not a whole decision-making workflow.

## What An Advanced Track Is Good For

Advanced tracks are good for reusable action blocks.

Examples:

```text
Prepare a form
Run a repeated cleanup action
Open a tool and arrange the window
Do a multi-step action that several sequences need
```

## Setup From Scratch

1. Create an advanced track with a clear action name.
2. Add only the steps that belong to that reusable action.
3. Test it by itself.
4. Save it.
5. Run it from a sequence with [Run Advanced Track](../Steps/Run-Advanced-Track.md) when needed.

Good names:

```text
PrepareReportWindow
FillCommonFields
CloseTemporaryPanels
```

## How It Differs From A Track

| Track | Advanced Track |
| --- | --- |
| Recorded input | Editable steps |
| Best for short actions | Best for reusable action blocks |
| Replays what you did | Lets you build a step list |
| Less flexible | More flexible |

## How It Differs From A Sequence

A sequence is the main workflow type for values, watchers, and recovery logic.

For background recovery checks, put the advanced track inside a sequence and add watchers there.

| Need | Use |
| --- | --- |
| Simple replay | Track |
| Reusable editable block | Advanced Track |
| Values, If steps, watchers, or recovery | Sequence |

## How Advanced Tracks Are Usually Used

You can run an advanced track directly.

You can also run one from a sequence with [Run Advanced Track](../Steps/Run-Advanced-Track.md).

Example:

```text
Sequence:
1. Run Advanced Track Prepare Report repeat 1
2. Wait For (Text) Ready timeout 30
3. Read Text statusText from selected status area
```

The advanced track does the reusable setup. The sequence decides what happens after that setup succeeds or fails.

## Return To Sequence

Inside an advanced track, [Return to Sequence](../Steps/Return-To-Sequence.md) hands control back to the sequence that called it.

Use it when an advanced track finishes early but the main sequence should continue.

## Good Advanced Track Design

- Keep it focused on one reusable action.
- Keep main workflow logic in the sequence that runs it.
- Use waits if the reusable action needs the app to become ready.
- Name it by what it does, not by where it was first used.
- If multiple sequences use it, avoid sequence-specific assumptions.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The advanced track contains too much workflow logic | Keep it focused on one reusable action and put decisions in a sequence |
| You need background recovery | Run the advanced track from a sequence and add watchers there |
| The next step runs too early | Add a wait or wait-for step after the advanced track changes the app |
| It works in one sequence but not another | Add setup steps before calling it, or remove assumptions about the window state |

## More About

- [Choosing What To Use](Choosing-What-To-Use.md)
- [Run Advanced Track](../Steps/Run-Advanced-Track.md)
- [Return to Sequence](../Steps/Return-To-Sequence.md)
- [Sequence](Sequence.md)
