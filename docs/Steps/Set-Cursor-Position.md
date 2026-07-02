# Set Cursor Position

Set Cursor Position moves the mouse cursor to a fixed screen position.

It does not click. Use it when the next step should press a mouse button at a known spot, or when you want to move the cursor away from something before continuing.

## Fields

| Field | Meaning |
| --- | --- |
| position | The screen position as `x,y` |
| Pick | Opens a fullscreen picker so you can click the position to use |

## Setup From Scratch

1. Add Set Cursor Position.
2. Click `Pick`.
3. Click the spot on the screen where the cursor should move.
4. Check that the position field now shows an `x,y` value.
5. Add the next step, such as [Press Mouse Button](Press-Mouse-Button.md), if you also want to click there.

## Example: Move Then Click

```text
1. Set Cursor Position 840,520
2. Press Mouse Button M1 hold 0.05 sec
```

## Example: Move Away Before Reading

If the cursor hover changes the target UI, move it away first:

```text
1. Set Cursor Position 20,20
2. Wait For (Text) Ready timeout 10
3. Read Text statusText from selected area
```

## Values Can Be Used

The position field can use a value if that value contains an `x,y` pair.

```text
Set Cursor Position {targetPoint}
```

## Useful For

- Moving the cursor to an exact point.
- Splitting mouse movement and mouse clicking into separate steps.
- Keeping the cursor away from hover-sensitive UI.
- Testing a fixed screen location before building a more flexible text or image click.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The cursor moves to the wrong place | Use `Pick` again while the target window is in the same position and display scale |
| The click happens but not at the expected point | Put Set Cursor Position immediately before Press Mouse Button |
| The position is invalid | Use `x,y`, for example `840,520` |
| The UI moves between runs | Use [Click Text](Click-Text.md) or [Click Image](Click-Image.md) instead of a fixed position |

## More About

- Pressing a mouse button: [Press Mouse Button](Press-Mouse-Button.md)
- Clicking visible text: [Click Text](Click-Text.md)
- Clicking an image target: [Click Image](Click-Image.md)
- Focus problems: [Wrong Window Or Focus](../Troubleshooting/Wrong-Window-Or-Focus.md)
