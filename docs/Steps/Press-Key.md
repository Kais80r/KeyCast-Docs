# Press Key

Press Key sends a keyboard key press or keyboard shortcut to the active app.

## Fields

| Field | Meaning |
| --- | --- |
| key | The key name or shortcut to press. Use `...` to capture a key or shortcut. |
| hold | How long to hold the key down |

## Setup From Scratch

1. Make sure the correct window is active.
2. Add Press Key.
3. Use `...` beside the key field and press the key or shortcut, or type the key name manually.
4. Use a small hold value for normal keys.

## Example: Save Shortcut

```text
1. Press Key Ctrl+S hold 0.05 sec
```

Example with focus and confirmation:

```text
1. Focus Window Report Tool
2. Press Key Ctrl+S hold 0.05 sec
3. Wait For (Text) Saved timeout 10
```

## Example: Plus Key

Use `Plus` when you want the plus key. Use `Ctrl+Plus` for shortcuts like browser zoom in. If your keyboard needs Shift for the plus character, the capture button can record it as `Shift+Plus`.

```text
1. Press Key Plus hold 0.05 sec
2. Press Key Ctrl+Plus hold 0.05 sec
```

## Example: Close Browser Tab

```text
1. Focus Window Edge
2. Press Key Ctrl+W hold 0.05 sec
```

## Example: Arrow Key

```text
1. Press Key ArrowDown hold 0.05 sec
```

## Example: Simple Key

```text
1. Press Key Enter hold 0.05 sec
```

## Useful For

- Keyboard shortcuts.
- Confirming dialogs.
- Navigation keys.
- Small input actions without a recorded track.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Keys go to the wrong app | Use [Focus Window](Focus-Window.md) before pressing keys |
| A shortcut is unreliable | Use [Click Text](Click-Text.md) when a visible target is more stable |
| A held key causes extra input | Shorten the hold time or use a normal key press |
| The next screen is not ready | Add a wait or wait-for step after shortcuts that open new screens |

## More About

- Focus troubleshooting: [Wrong Window Or Focus](../Troubleshooting/Wrong-Window-Or-Focus.md)
- Focusing a window first: [Focus Window](Focus-Window.md)
- Waiting for a window: [Wait For (Window)](Wait-For.md)
- Clicking text instead of pressing keys: [Click Text](Click-Text.md)
- Recorded keyboard actions: [Play Track](Play-Track.md)