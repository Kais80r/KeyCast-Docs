# When Window

Use When Window when the watcher should react to a window or application state.

This is useful when a workflow can be interrupted by another window, a dialog, or a focus change.

Use window triggers for window-level state. If you need to know whether the content inside the window is ready, use text or image checks too.

## Good Uses

- A confirmation window opens.
- A login window appears.
- The wrong app becomes active.
- A required window is missing.

## Setup Example

```text
Watcher trigger:
When Window Settings is visible

Watcher steps:
1. Pause Sequence
2. Press key Escape
3. Jump Sequence Step 3
```

## Window Trigger Versus Window Step

| Need | Use |
| --- | --- |
| React if a window appears while work is running | When Window watcher trigger |
| Wait in the normal path until a window exists | [Wait For (Window)](../../Steps/Wait-For.md) |
| Branch once based on a window state | [If Window](../../Steps/If-Window.md) |
| Bring a window forward | [Focus Window](../../Steps/Focus-Window.md) |

## Tips

- Use a clear part of the window title.
- Avoid titles that change constantly.
- If focus matters, test with the app in the same state you expect during playback.
- Combine with Pause Sequence when the main path must stop until the window is handled.

## More About

- [Wait For (Window)](../../Steps/Wait-For.md)
- [If Window](../../Steps/If-Window.md)
- [Focus Window](../../Steps/Focus-Window.md)
- [Wrong Window Or Focus](../../Troubleshooting/Wrong-Window-Or-Focus.md)
