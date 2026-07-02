# Crash Protection

Crash Protection stops playback if a selected window or app closes.

It is meant as a safety feature. If the app you depend on disappears, WhirlyTask stops instead of continuing to send keys or clicks into the wrong place.

## Where To Find It

Open:

```text
Menu > Crash Protection
```

The menu shows:

- `Off`
- available windows/apps
- `Discord Message`

## Setup

1. Open the app or window you want to protect.
2. Open WhirlyTask.
3. Open `Menu > Crash Protection`.
4. Choose the window/app from the list.
5. Run playback normally.

If that selected window/app closes during playback, WhirlyTask stops playback and shows:

```text
Crash Protection stopped playback.
```

## Discord Alert

Crash Protection can also send a Discord message.

To use it:

1. Set a webhook in [Discord Webhook](Discord-Webhook.md).
2. Open `Menu > Crash Protection`.
3. Turn on `Discord Message`.

When Crash Protection stops playback, WhirlyTask sends a protection alert.

## When To Use It

Use Crash Protection when:

- The workflow depends on one main app staying open.
- Keyboard or mouse playback would be unsafe if the app closed.
- A closed target should stop all automation immediately.

## Crash Protection Versus Watchers

| Feature | Best for |
| --- | --- |
| Crash Protection | Stop playback when a selected app/window closes |
| Watcher | React to text, images, values, windows, chance, or internet state inside a sequence |

Crash Protection is global and simple. Watchers are more flexible but only exist inside sequences.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The target window is not listed | Open the window first, then choose it from Crash Protection |
| Playback stops before the workflow starts | Make sure the protected window stays open while playback begins |
| Protection stops matching the app | Re-select the target after the app restarts or changes window state |
| Discord alert does not send | Set up [Discord Webhook](Discord-Webhook.md) before enabling the alert |

## Tips

- Choose the most important app/window, not a temporary dialog.
- Use [Focus Window](../Steps/Focus-Window.md) or [Wait For (Window)](../Steps/Wait-For.md) in sequences when focus or window state also matters.
- Turn Crash Protection off when testing workflows that intentionally close the protected window.
