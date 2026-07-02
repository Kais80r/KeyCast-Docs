# Track

A track is a recorded keyboard and mouse action.

Use a track when you want WhirlyTask to replay something you already did by hand.

Think of a track as a recording. It is fast to create and replays the input exactly as recorded.

## What A Track Is Good For

Tracks are best for simple, stable actions.

Examples:

```text
Click a fixed button
Press a shortcut
Fill a small group of fields
Open a menu and choose an item
```

## Setup From Scratch

1. Put the target app or window in the same state you want to start from later.
2. Record the keyboard and mouse action.
3. Stop recording as soon as the action is finished.
4. Save the track with a clear name.
5. Play it once while watching where the input goes.

Good names describe the action:

```text
OpenSettings
FillHeaderFields
ConfirmDialog
```

## What A Track Is Not Good For

A plain track is best when the screen starts in the same state each time.

If the target moves, a popup appears, or the workflow needs to decide what to do next, use a sequence.

Use a sequence when you need:

- If steps.
- Values.
- Read Text.
- Watchers.
- Retry logic.
- Loops.
- Recovery from unexpected states.

## When A Track Starts Failing

If a track works once but fails later, the starting state probably changed.

Common fixes:

| Problem | Fix |
| --- | --- |
| Keys go to the wrong app | Use [Focus Window](../Steps/Focus-Window.md) before playing the track |
| The app is still loading | Use [Wait For (Text)](../Steps/Wait-For.md) or [Wait For (Window)](../Steps/Wait-For.md) |
| A popup appears sometimes | Use a [sequence watcher](../Watchers/README.md) |
| One recorded track is too large | Split it into smaller tracks or advanced tracks |

## How Tracks Are Usually Used

You can play a track directly from the main window.

You can also run a track from a sequence with [Play Track](../Steps/Play-Track.md).

Example:

```text
Sequence:
1. Focus Window Report Tool
2. Play Track Fill Date Fields repeat 1
3. Wait For (Text) Ready timeout 30
```

The sequence handles the setup and checks. The track handles the simple repeated input.

## Good Track Design

- Keep tracks short.
- Record only one clear action.
- Make sure the target window is in the same state before replaying.
- Use a sequence around the track if setup or recovery is needed.
- Prefer stable keyboard shortcuts when possible.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Clicks land in the wrong place | Put the window in the same position, or use a sequence with [Click Text](../Steps/Click-Text.md) or [Click Image](../Steps/Click-Image.md) |
| Keys go to the wrong window | Use [Focus Window](../Steps/Focus-Window.md) before playing the track |
| The app is not ready | Use [Wait For (Window)](../Steps/Wait-For.md) or [Wait For (Text)](../Steps/Wait-For.md) before the track |
| The track has too many unrelated actions | Split it into shorter tracks or advanced tracks |

## More About

- [Choosing What To Use](Choosing-What-To-Use.md)
- [Play Track](../Steps/Play-Track.md)
- [Recording Options](../App-Features/Recording-Options.md)
- [Wrong Window Or Focus](../Troubleshooting/Wrong-Window-Or-Focus.md)
