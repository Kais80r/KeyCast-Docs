# App Features

This folder explains WhirlyTask features that are not individual sequence steps.

These features live around the main app, menu, recording system, playback system, and global safety settings.

Use this folder when the thing you want is controlled from the main WhirlyTask menu instead of from an Add Step row inside a sequence.

## Find A Feature By Goal

| I want to... | Open |
| --- | --- |
| Stop playback if a selected app or window closes | [Crash Protection](Crash-Protection.md) |
| Stop playback if specific text appears | [Text Protection](Text-Protection.md) |
| Send messages to Discord | [Discord Webhook](Discord-Webhook.md) |
| Change record, play, stop, or emergency hotkeys | [Hotkeys](Hotkeys.md) |
| Control what gets recorded into tracks | [Recording Options](Recording-Options.md) |
| Save OCR screenshots and reports while testing text reading | [OCR Debug Captures](OCR-Debug-Captures.md) |
| Change playback speed or looping | [Playback, Speed, And Loop](Playback-Speed-And-Loop.md) |
| Load, save, and manage saved items | [Library And Files](Library-And-Files.md) |
| Understand Save, Save New, and Cancel | [Editors And Saving](Editors-And-Saving.md) |
| Keep WhirlyTask visible or open these docs | [Always On Top And Help](Always-On-Top-And-Help.md) |

## Feature Pages

| Feature | What it explains |
| --- | --- |
| [Crash Protection](Crash-Protection.md) | Stop playback if a selected window/app closes |
| [Text Protection](Text-Protection.md) | Stop playback if selected text appears on screen |
| [Discord Webhook](Discord-Webhook.md) | Set up Discord output for messages and protection alerts |
| [Hotkeys](Hotkeys.md) | Change Record, Play, Stop, and Emergency keys |
| [Recording Options](Recording-Options.md) | Choose what gets recorded into tracks |
| [OCR Debug Captures](OCR-Debug-Captures.md) | Save OCR screenshots and reports while testing text reading |
| [Playback, Speed, And Loop](Playback-Speed-And-Loop.md) | Playback speed and continuous track playback |
| [Library And Files](Library-And-Files.md) | Save/load tracks, advanced tracks, and sequences |
| [Editors And Saving](Editors-And-Saving.md) | How editor Save, Save New, and Cancel behave |
| [Always On Top And Help](Always-On-Top-And-Help.md) | Window pinning and opening documentation |

## App Features Versus Steps

| Thing | Where to learn |
| --- | --- |
| A step inside a sequence | [Steps](../Steps/README.md) |
| A watcher inside a sequence | [Watchers](../Watchers/README.md) |
| A global playback safety setting | This folder |
| A saved item type | [Basics](../Basics/README.md) |

## Protections Versus Watchers

Crash Protection and Text Protection are simple global safety settings. They stop playback.

Watchers are sequence-specific and can run custom steps.

| Need | Use |
| --- | --- |
| Stop immediately when a selected app closes | Crash Protection |
| Stop immediately when a phrase appears | Text Protection |
| Click, wait, recover, message, or continue after a condition | Watcher |

## Useful Starting Points

- If playback should stop when a monitored app closes, use [Crash Protection](Crash-Protection.md).
- If playback should stop when specific text appears, use [Text Protection](Text-Protection.md).
- If messages should go to Discord, set up [Discord Webhook](Discord-Webhook.md).
- If recorded tracks include too much mouse movement, check [Recording Options](Recording-Options.md).
- If screen text is hard to diagnose, turn on [OCR Debug Captures](OCR-Debug-Captures.md).

## More About

- [Getting Started](../Getting-Started.md)
- [Steps](../Steps/README.md)
- [Watchers](../Watchers/README.md)
- [Troubleshooting](../Troubleshooting/README.md)
