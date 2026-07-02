# When Internet

Use When Internet when the watcher should react to a connection state.

This is useful for workflows that depend on a network connection or online page.

Internet state tells you whether a connection is available. Use text, image, or window checks for app, page, or server readiness.

## Good Uses

- Stop or pause when the connection drops.
- Show a notification when the connection returns.
- Wait before continuing a network-based task.

## Setup Example

```text
Watcher trigger:
When Internet is disconnected

Watcher steps:
1. Pause Sequence
2. Status Message Connection lost
3. Wait 10 seconds
4. Reset and Restart Sequence
```

## When To Combine It With Other Checks

Use internet state for the broad connection problem.

Use text, image, or window checks for app-specific readiness.

Example:

```text
Watcher:
When Internet is disconnected
1. Pause Sequence
2. Wait 10 seconds
3. Reset and Restart Sequence

Main steps:
Wait For (Text) Loaded
```

## Tips

- Use a longer cooldown to avoid repeated recovery.
- Combine internet state with app-specific checks when the app itself can be slow.
- Combine with Wait For (Text) when a page also shows a loaded status.

## More About

- [Wait For (Internet)](../../Steps/Wait-For.md)
- [If Internet](../../Steps/If-Internet.md)
- [Wait For (Text)](../../Steps/Wait-For.md)
