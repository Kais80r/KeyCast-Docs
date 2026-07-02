# When Image

Use When Image when the watcher should react to a visual target instead of readable text.

This is useful for icons, symbols, buttons without readable text, or visual states that stay consistent.

Use an image trigger when text reading is not the right tool. If the visible thing has clear text, a text trigger is often easier to understand and maintain. Use `...` beside the Image field to browse for the image file.

## Good Image Targets

- A stable icon.
- A unique button image.
- A clear status symbol.
- A stable part of the interface.

## Risky Image Targets

- Large empty areas.
- Text that changes.
- Animated highlights.
- Blinking cursors.
- Crops with changing numbers.
- Targets that are partly covered by another window.

## Setup Example

```text
Watcher trigger:
When Image warning-icon is found in selected area

Watcher steps:
1. Status Message Warning icon appeared
2. Click Image warning-icon
```

If the image means the normal sequence should stop:

```text
Watcher steps:
1. Stop Sequence
```

If the image means the watcher should recover:

```text
Watcher steps:
1. Pause Sequence
2. Click Image warning-icon
3. Jump Sequence Step 3
```

## Tips

- Crop only the stable part of the target.
- Keep the same display scaling when testing.
- Use a selected area if the icon appears in a known place.
- If matching is unreliable, recapture the image target.

## More About

- [Click Image](../../Steps/Click-Image.md)
- [If Image](../../Steps/If-Image.md)
- [Image Not Found](../../Troubleshooting/Image-Not-Found.md)
- [Making Areas Reliable](../../Tips/Making-Areas-Reliable.md)
