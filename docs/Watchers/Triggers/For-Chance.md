# For Chance

Use For Chance when a watcher should only fire sometimes instead of every time.

This is an advanced trigger. Most workflows should use text, image, value, window, or internet triggers first.

Chance is not a safety check. It is for optional behavior.

## Good Uses

- Occasional checks.
- Randomized optional behavior.
- Testing whether a watcher path works without forcing it every run.

## Avoid It For

- Error recovery.
- Crash or safety behavior.
- Required waits.
- Anything that must happen every time.

For required logic, use a real condition such as text, image, window, value, or internet state.

## Setup Example

```text
Watcher trigger:
For Chance 10%

Watcher steps:
1. Status Message Optional check ran
```

## Tips

- Keep the chance easy to understand.
- Use Status Message while testing.
- Use a real condition for important recovery logic, such as text, image, window, value, or internet state.

## More About

- [Watcher Triggers](README.md)
- [Keeping Watchers Predictable](../../Tips/Keeping-Watchers-Predictable.md)
