# Press Mouse Button

Press Mouse Button presses one mouse button at the cursor's current position.

It does not move the cursor first. Use [Set Cursor Position](Set-Cursor-Position.md), [Click Text](Click-Text.md), or [Click Image](Click-Image.md) when the cursor needs to move to a target first.

## Fields

| Field | Meaning |
| --- | --- |
| Mouse | Which mouse button to press: `M1` left, `M2` right, `M3` wheel click, `M4` back, or `M5` forward |
| hold | Seconds to hold the button down |

## Setup From Scratch

1. Add Press Mouse Button.
2. Choose the mouse button: `M1`, `M2`, `M3`, `M4`, or `M5`.
3. Use a short hold value for a normal click, such as `0.05`.
4. Add Set Cursor Position before it if the click should happen at a fixed screen point.

## Example: Left Click Current Position

```text
1. Press Mouse Button M1 hold 0.05 sec
```

## Example: Move Then Right Click

```text
1. Set Cursor Position 840,520
2. Press Mouse Button M2 hold 0.05 sec
```

## Mouse Button Names

| Button | Meaning |
| --- | --- |
| `M1` | Left mouse button |
| `M2` | Right mouse button |
| `M3` | Middle mouse button / wheel click |
| `M4` | First side button / back |
| `M5` | Second side button / forward |

## Useful For

- Clicking at a cursor position set by a previous step.
- Pressing side mouse buttons.
- Holding a mouse button briefly.
- Building mouse actions that are easier to edit than a recorded track.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The click happens in the wrong place | Add Set Cursor Position immediately before Press Mouse Button |
| The app reacts like a drag | Shorten the hold value |
| Nothing happens | Make sure the target window is focused and the cursor is over the target |
| The target moves between runs | Use [Click Text](Click-Text.md) or [Click Image](Click-Image.md) instead |

## More About

- Moving the cursor first: [Set Cursor Position](Set-Cursor-Position.md)
- Clicking text directly: [Click Text](Click-Text.md)
- Clicking image targets: [Click Image](Click-Image.md)
- Pressing keyboard keys: [Press Key](Press-Key.md)
