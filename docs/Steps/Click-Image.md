# Click Image

Click Image searches the current screen for an image target and clicks the center of the match, plus any offset you enter.

## Fields

| Field | Meaning |
| --- | --- |
| Image | The image file or image target to find. Use `...` to browse for an image file. |
| Area | Where to search for the image target |
| delay | Seconds to wait before clicking |
| hold | Seconds to hold the selected mouse button. Use `0` to move to the target without clicking. |
| Mouse | Which mouse button to click: `M1` left, `M2` right, `M3` wheel click, `M4` back, or `M5` forward. |
| Offset | Extra `x,y` movement from the found center |

## Setup From Scratch

1. Capture or choose an image target.
2. Add Click Image.
3. Use `...` beside the Image field to browse for the image file, or type/paste the path.
4. Start with Full Screen for testing.
5. Use a selected area if the image appears in one known place.
6. Choose the Mouse button to click: `M1`, `M2`, `M3`, `M4`, or `M5`. Set hold to `0` when you only want to move the mouse to the target.
7. Leave Offset as `0,0` to click the center of the matched image.
8. Use Offset when the click should land next to the matched image.

## Example

```text
1. Click Image save-icon from selected toolbar area
```

Example with response check:

```text
1. Click Image save-icon from selected toolbar area
2. Wait For (Text) Saved timeout 10
```

## Example: Click Beside An Image

If the image is a stable marker near the real button, use Offset to move from the matched image center to the click target.

```text
Click Image warning-icon from selected dialog area
Offset: 60,0
```

## Good Image Targets

- Stable icons.
- Static button artwork.
- Unique symbols.
- A stable part of the UI.

## Bad Image Targets

- Changing numbers.
- Animated effects.
- Hover highlights.
- Large blank areas.
- Text that changes between runs.

## Useful For

- Icons without readable labels.
- Visual status buttons.
- Controls where text reading is unreliable.
- Unique symbols in a stable area.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The image is not found | Capture only the stable part of the target with a little surrounding context |
| Matching works once and then fails | Avoid target images that include changing text, counters, or animation frames |
| Matching fails after display changes | Keep the same display scale and window size used when the target was captured |
| The wrong copy is clicked | Search a selected area instead of Full Screen |
| The image is found but the click lands slightly off | Adjust Offset. `0,0` means the center of the matched image |

## More About

- Image troubleshooting: [Image Not Found](../Troubleshooting/Image-Not-Found.md)
- Waiting for an image: [Wait For (Image)](Wait-For.md)
- Image conditions: [If Image](If-Image.md)
- Reliable selected areas: [Making Areas Reliable](../Tips/Making-Areas-Reliable.md)
- Text targets instead of image targets: [Click Text](Click-Text.md)
