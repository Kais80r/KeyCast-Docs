# Getting Started

Start here if you are new to WhirlyTask or if you are not sure what kind of saved item to build.

WhirlyTask can record input, run editable step lists, read text from the screen, store values, send messages, and react to problems while a workflow is running. The easiest way to build something reliable is to start small, then add logic only when the workflow actually needs it.

## The Short Version

| If you want to... | Use |
| --- | --- |
| Replay a simple action you already did by hand | [Track](Basics/Track.md) |
| Reuse an editable action block in multiple places | [Advanced Track](Basics/Advanced-Track.md) |
| Build a workflow with decisions, values, reading, loops, or recovery | [Sequence](Basics/Sequence.md) |
| Watch for unexpected text, images, windows, values, or connection changes | [Watcher](Watchers/README.md) inside a sequence |

Most larger automations become a sequence. Tracks and advanced tracks are still useful because a sequence can run them as smaller building blocks.

## A Good First Build

Start with one small path before building the full final automation.

1. Make the app or window look the way it should look before the automation starts.
2. Create a small track or sequence with only the first few actions.
3. Add a [Status Message](Steps/Status-Message.md) so you can see where the workflow is.
4. Run it once.
5. Fix timing, focus, or selected area problems.
6. Add the next small part.
7. Save the editor before closing it.

This keeps problems easier to find. If ten new steps are added at once, it is harder to know which one caused the problem.

## How A Sequence Is Usually Built

A sequence has three main areas:

| Area | What goes there |
| --- | --- |
| Starting Values | Named pieces of text or numbers the sequence can use |
| Main Steps | The normal path that should happen when nothing goes wrong |
| Watchers | Background checks for unexpected events, safety, or recovery |

Good sequence structure:

```text
Starting Values:
statusText starts as empty
attempts starts as 0

Main Steps:
1. Do the normal workflow
2. Read or wait for the result
3. Continue, loop, send a message, or stop

Watchers:
When an unexpected problem appears:
1. Pause Sequence
2. Handle the problem
3. Go back, reset and restart, or stop
```

## What To Add First

| Need | Add this first |
| --- | --- |
| The workflow is too fast | [Wait](Steps/Wait.md) or [Wait For (Text)](Steps/Wait-For.md) |
| Keys or clicks go to the wrong app | [Focus Window](Steps/Focus-Window.md) |
| The workflow depends on visible text | [Wait For (Text)](Steps/Wait-For.md), [If Text](Steps/If-Text.md), or [Read Text](Steps/Read-Text.md) |
| You need to remember text or a counter | [Values](Values/README.md) |
| You need to stop after too many repeats | [Counter Limit](Examples/Counter-Limit.md) |
| Something unexpected can appear | [Watchers](Watchers/README.md) |
| You need messages outside WhirlyTask | [Discord Webhook](App-Features/Discord-Webhook.md) and [Discord Message](Steps/Discord-Message.md) |
| Playback must stop if the target app closes | [Crash Protection](App-Features/Crash-Protection.md) |
| Playback must stop if dangerous text appears | [Text Protection](App-Features/Text-Protection.md) |

## Screen Text Reading

WhirlyTask can read visible text from the screen. The technical word for this is OCR, but in these docs it is usually called screen text reading.

Use screen text reading when the app shows information that the automation needs to use later.

Common pattern:

```text
Starting Values:
resultText starts as empty

Main Steps:
1. Read Text resultText from selected area
2. Status Message Read: {resultText}
3. If Sequence Value resultText contains Complete
```

Read Text stores the detected text in the value you choose. Other text boxes can then use that value with braces, for example `{resultText}`.

More detail:

- [Read Text](Steps/Read-Text.md)
- [Reading Text Into Values](Values/Reading-Text-Into-Values.md)
- [Making Areas Reliable](Tips/Making-Areas-Reliable.md)
- [Read Text Is Wrong](Troubleshooting/Read-Text-Is-Wrong.md)

## Watchers Are For Side Events

Use main steps for the normal path. Use watchers for things that can happen at unexpected times.

Examples:

```text
Normal path:
Wait for Complete, then continue

Watcher:
If Error appears, pause the sequence and recover
```

By default, a watcher runs alongside the main sequence. If the watcher should take control, put [Pause Sequence](Steps/Pause-Sequence.md) near the start of the watcher steps. Then end the watcher with a continuation step, such as [Jump Sequence Step](Steps/Jump-Sequence-Step.md), [Reset and Restart Sequence](Steps/Reset-And-Restart-Sequence.md), or [Stop Sequence](Steps/Stop-Sequence.md).

## A Simple Reliability Checklist

Before building a large workflow, check these:

| Question | Why it matters |
| --- | --- |
| Is the right window focused? | Keys and clicks go wherever focus is |
| Is the screen area a little bigger than the text or image? | Tight areas can cut off important pixels |
| Does the step work by itself? | Isolated tests make bugs easier to find |
| Are value names spelled exactly the same everywhere? | `{statusText}` and `{statustext}` are different |
| Does every watcher that pauses also continue or stop? | A paused sequence needs a clear next action |
| Did you press Save before closing the editor? | Closing cancels unsaved editor changes |

## Where To Go Next

| If you want... | Open |
| --- | --- |
| Definitions of WhirlyTask words | [Glossary](Glossary.md) |
| A deeper choice between item types | [Choosing What To Use](Basics/Choosing-What-To-Use.md) |
| A list of every step | [Steps](Steps/README.md) |
| Complete patterns to copy | [Examples](Examples/README.md) |
| Practical building habits | [Tips](Tips/README.md) |
| Fixes for common problems | [Troubleshooting](Troubleshooting/README.md) |
