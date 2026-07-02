# Text Clicks Wrong Place

This page is for Click Text clicking the wrong match or clicking the right text but landing in the wrong spot.

## Why It Happens

The same text may appear more than once, the text reader may find a similar word somewhere else, or the Offset may move the click away from the found center.

## Fixes

- Use a selected area around the correct target.
- Match a longer phrase if it is unique.
- Match a shorter phrase if the full text is read inconsistently.
- Keep Offset at `0,0` when you want to click the center of the found text.
- Adjust Offset only when the click should land beside the text.
- Test Read Text on the same area to see what WhirlyTask sees.
- If the target is an icon or stylized button, use Click Image.

## Example

Instead of:

```text
Click Text OK from Full Screen
```

Use:

```text
Click Text OK from selected dialog area
Offset: 0,0
```

## More About

- Click Text step: [Click Text](../Steps/Click-Text.md)
- Wait For (Text) step: [Wait For (Text)](../Steps/Wait-For.md)
- Selected area problems: [Selected Area Problems](Selected-Area-Problems.md)
- Making areas reliable: [Making Areas Reliable](../Tips/Making-Areas-Reliable.md)
- Image targets: [Click Image](../Steps/Click-Image.md)
