# Text Protection

Text Protection stops playback when WhirlyTask sees specific text on the screen.

It is a global safety feature. It is useful when certain visible text means playback should stop immediately.

## Where To Find It

Open:

```text
Menu > Text Protection
```

The menu shows:

- `Off`
- `Set Text...`
- the current protected text when enabled
- `Discord Message`

## Setup

1. Open `Menu > Text Protection > Set Text...`.
2. Enter the text that should stop playback.
3. Start playback.

If WhirlyTask sees that text, playback stops and the status shows:

```text
Text Protection stopped playback.
```

## How It Checks

Text Protection uses screen text reading. The technical word is OCR.

It checks when playback starts and then checks again during playback at random intervals. This keeps it from scanning constantly while still catching the protected text.

## Discord Alert

Text Protection can also send a Discord message.

To use it:

1. Set a webhook in [Discord Webhook](Discord-Webhook.md).
2. Open `Menu > Text Protection`.
3. Turn on `Discord Message`.

When Text Protection stops playback, WhirlyTask sends a protection alert.

## When To Use It

Use Text Protection when:

- A warning phrase means automation should stop.
- A failure message can appear during playback.
- You need a simple global stop rule without building a watcher.

## Text Protection Versus Wait For (Text)

| Feature | Best for |
| --- | --- |
| Text Protection | Stop playback if text appears at any time |
| Wait For (Text) | Pause one sequence step until text appears |
| Watcher When Text | Run custom recovery steps when text appears |

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Protected text is not detected | Use a short, clear phrase and test the same text with [Read Text](../Steps/Read-Text.md) |
| Playback stops on harmless text | Use a more specific phrase, or use a watcher when you need custom context |
| The exact phrase is missed | Match the most stable part of the message instead of the full sentence |
| Text appears only briefly | Use a watcher if the text needs custom timing or recovery steps |
| Discord alert does not send | Set up [Discord Webhook](Discord-Webhook.md) before enabling the alert |

## Tips

- Use a short, unique phrase.
- Avoid generic words that appear often.
- If you need custom handling instead of stopping, use a [watcher](../Watchers/README.md).
- If screen text is not read correctly, see [Read Text Is Wrong](../Troubleshooting/Read-Text-Is-Wrong.md).
