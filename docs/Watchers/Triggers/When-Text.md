# When Text

Use When Text when a watcher should react to words or numbers visible on the screen.

The app reads the screen and checks whether the selected text condition is true.

Use this for text that may appear while the main sequence is doing other work. If the normal next step is simply waiting for text, [Wait For (Text)](../../Steps/Wait-For.md) in the main steps is usually clearer.

## Good Uses

- A status label appears.
- A popup message appears.
- A button or heading becomes visible.
- A result changes to a known word.

## Area Choice

| Area | Use when |
| --- | --- |
| Full Screen | The text can appear in different places |
| Selected area | The text appears in one stable place |

Selected areas are faster and less noisy, but they must include the full text with a little space around it.

## Setup Example

```text
Watcher trigger:
When Text Complete is seen from selected area every 2 seconds

Watcher steps:
1. Status Message Complete appeared
```

If the watcher should interrupt the main sequence:

```text
Watcher steps:
1. Pause Sequence
2. Click Text OK
3. Jump Sequence Step 4
```

## Tips

- Use a short, unique piece of text.
- Avoid text that appears in many places.
- Make the selected area slightly larger than the letters.
- If the app reads the text wrong, test Read Text on the same area.
- If text is stylized or tiny, a larger area often reads better.

## More About

- Text reading problems: [Read Text Is Wrong](../../Troubleshooting/Read-Text-Is-Wrong.md)
- Selected areas: [Selected Area Problems](../../Troubleshooting/Selected-Area-Problems.md)
- Taking over: [Pause Sequence](../Steps/Pause-Sequence.md)
