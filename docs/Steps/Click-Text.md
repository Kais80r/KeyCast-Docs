# Click Text

Click Text searches the current screen for visible text and clicks the center of the text box it found, plus any offset you enter.

## Fields

| Field | Meaning |
| --- | --- |
| Text | The text to find |
| Area | Where to search for the text |
| delay | Seconds to wait before clicking |
| hold | Seconds to hold the selected mouse button. Use `0` to move to the target without clicking. |
| Mouse | Which mouse button to click: `M1` left, `M2` right, `M3` wheel click, `M4` back, or `M5` forward. |
| Offset | Extra `x,y` movement from the found center |

## Setup From Scratch

1. Add Click Text.
2. Enter the visible text you want to click.
3. Start with Full Screen if you are testing.
4. Switch to a selected area if there are multiple matches.
5. Choose the Mouse button to click: `M1`, `M2`, `M3`, `M4`, or `M5`. Set hold to `0` when you only want to move the mouse to the target.
6. Leave Offset as `0,0` for normal buttons and menu items.
7. Use Offset when the click should land beside the found text instead of directly on its center.

## Example: Click A Button

```text
1. Click Text Submit from selected dialog area
```

Example with response check:

```text
1. Click Text Submit from selected dialog area
2. Wait For (Text) Complete timeout 30
```

## Example: Click Beside Text

Some interfaces have a label and a clickable control beside it. Click Text starts from the center of the found text. Use Offset to move the click onto the nearby control.

```text
Click Text Username from selected form area
Offset: 80,0
```

Use negative values to move left or up:

```text
Offset: -40,-10
```

## Text Can Use Values

The text field can include a value:

```text
Click Text {buttonText}
```

This is useful when the target text was read or set earlier.

## Useful For

- Buttons with readable labels.
- Tabs or menu items.
- Form controls next to labels.
- Dialog actions.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The wrong copy of the text is clicked | Use a selected area around the correct copy |
| Text is matched in an unrelated place | Narrow the search area to the part of the screen that matters |
| The click lands beside the target | Adjust Offset. `0,0` means the center of the found text |
| A stylized icon is not clicked reliably | Use [Click Image](Click-Image.md) instead |
| Text is not found | Make the selected area larger so the letters are not cut off |

## More About

- Text click troubleshooting: [Text Clicks Wrong Place](../Troubleshooting/Text-Clicks-Wrong-Place.md)
- Reliable selected areas: [Making Areas Reliable](../Tips/Making-Areas-Reliable.md)
- Waiting for text first: [Wait For (Text)](Wait-For.md)
- Using values as target text: [Using Values In Text Boxes](../Tips/Using-Values-In-Text-Boxes.md)
- Image targets: [Click Image](Click-Image.md)
