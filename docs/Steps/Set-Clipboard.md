# Set Clipboard

Set Clipboard replaces the Windows clipboard text.

## Fields

| Field | Meaning |
| --- | --- |
| Text | Text to put into the clipboard |

## Setup From Scratch

1. Add Set Clipboard.
2. Enter the text to copy.

## Example: Plain Text

```text
1. Set Clipboard Report complete
```

Example with paste:

```text
1. Set Clipboard Report complete
2. Focus Window Report Tool
3. Press Key Ctrl+V
```

## Example: Value Text

```text
1. Read Text statusText from selected status area
2. Set Clipboard Current status: {statusText}
3. Press Key Ctrl+V
```

## Useful For

- Pasting text into fields.
- Reusing text read from the screen.
- Avoiding long typed input.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The previous clipboard content is replaced | Use this step only when changing the real clipboard is expected |
| Text pastes into the wrong window | Focus the target window before pasting |
| A placeholder becomes blank | Fill the value before Set Clipboard runs |

## More About

- Using values in text boxes: [Using Values In Text Boxes](../Tips/Using-Values-In-Text-Boxes.md)
- Reading text into a value: [Read Text](Read-Text.md)
- Values: [Values](../Values/README.md)
- Focusing the right window before pasting: [Focus Window](Focus-Window.md)
- Focus troubleshooting: [Wrong Window Or Focus](../Troubleshooting/Wrong-Window-Or-Focus.md)
