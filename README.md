# WhirlyTask Documentation

WhirlyTask is a Windows automation app for building keyboard, mouse, screen-text reading, image matching, notification, and watcher-based workflows without writing scripts.

This documentation is written for general desktop automation. The examples use neutral cases such as forms, dashboards, reports, popups, status labels, and repeated app tasks so the same ideas can be reused in many different workflows.

![WhirlyTask flow overview](docs/assets/diagrams/whirlytask-automation-flow.svg?v=smart-playback-helpers)

## Start Here

If you are new, read these in order:

1. [Getting Started](docs/Getting-Started.md)
2. [Choosing What To Use](docs/Basics/Choosing-What-To-Use.md)
3. [Build A Reliable Sequence](docs/Guides/Build-A-Reliable-Sequence.md)
4. [Values](docs/Values/README.md) if you need to remember text, numbers, or results
5. [Watchers](docs/Watchers/README.md) if you need background checks or recovery
6. [Troubleshooting](docs/Troubleshooting/README.md) when something does not work

If you already know what you need, use the table below.

## Find What You Need

| I want to... | Start here |
| --- | --- |
| Learn the basic workflow | [Getting Started](docs/Getting-Started.md) |
| Understand WhirlyTask words | [Glossary](docs/Glossary.md) |
| Understand tracks, advanced tracks, and sequences | [Basics](docs/Basics/README.md) |
| Build a system from scratch | [Guides](docs/Guides/README.md) |
| Set up protections, Discord, hotkeys, recording, or loop playback | [App Features](docs/App-Features/README.md) |
| Fix something that does not work | [Troubleshooting](docs/Troubleshooting/README.md) |
| Choose or understand a step | [Steps](docs/Steps/README.md) |
| Run background recovery logic | [Watchers](docs/Watchers/README.md) |
| Store, read, or change values | [Values](docs/Values/README.md) |
| Build loops, retries, and notification systems | [Examples](docs/Examples/README.md) |
| Build cleaner and more reliable automations | [Tips](docs/Tips/README.md) |
| Read text from the screen | [Read Text](docs/Steps/Read-Text.md) |
| Learn why a selected area fails | [Selected Area Problems](docs/Troubleshooting/Selected-Area-Problems.md) |
| See all documentation sections | [Docs Index](docs/README.md) |

## What WhirlyTask Is Good At

WhirlyTask is useful when a workflow has repeatable input or visible screen states:

- Repeating keyboard and mouse actions.
- Waiting for visible text, images, windows, or network state.
- Reading visible screen text into named values. The technical word for this is OCR.
- Clicking UI text or image targets.
- Sending notifications with live values.
- Recovering from popups, errors, focus changes, or missing states.
- Combining normal steps with background watchers.

## Common Starting Points

| Situation | Best starting point |
| --- | --- |
| You only need to replay a recorded action | [Track](docs/Basics/Track.md) |
| You want a reusable action block | [Advanced Track](docs/Basics/Advanced-Track.md) |
| You need decisions, loops, values, or watchers | [Sequence](docs/Basics/Sequence.md) |
| You need to read visible text | [Read Text](docs/Steps/Read-Text.md) |
| You need a screen text workflow | [Screen Text Reading Workflow](docs/Guides/Screen-Text-Reading-Workflow.md) |
| You need to send Discord alerts | [Discord Webhook](docs/App-Features/Discord-Webhook.md) |
| You need the workflow to recover from problems | [Watcher Recovery](docs/Examples/Watcher-Recovery.md) |
| You need a loop with a stop limit | [Counter Limit](docs/Examples/Counter-Limit.md) |

## How The Docs Are Organized

The documentation is split into folders so each topic has its own page:

- Use [Getting Started](docs/Getting-Started.md) when you want the full beginner path.
- Use [Basics](docs/Basics/README.md) first if you are not sure what a track, advanced track, or sequence is.
- Use [Guides](docs/Guides/README.md) when you want a full setup explanation.
- Use [App Features](docs/App-Features/README.md) for protection settings, Discord setup, recording options, hotkeys, and playback controls.
- Use [Steps](docs/Steps/README.md) when you need to know what a specific step does.
- Use [Watchers](docs/Watchers/README.md) when you need background checks or recovery logic.
- Use [Values](docs/Values/README.md) when you need to store and reuse text.
- Use [Examples](docs/Examples/README.md) when you want complete setup patterns.
- Use [Tips](docs/Tips/README.md) when you want practical advice for building reliable automations.
- Use [Troubleshooting](docs/Troubleshooting/README.md) when something does not work.
