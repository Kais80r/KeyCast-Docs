# Read Text Is Wrong

This page is for cases where Read Text returns strange letters, missing punctuation, wrong numbers, or broken words.

## Why It Happens

Read Text looks at an image of the screen and guesses the letters. Small areas, stylized fonts, shadows, icons, and outlines can make that harder.

Common symptoms:

| Symptom | Likely cause |
| --- | --- |
| `0` becomes `O` | Number and letter look similar |
| A dot disappears | The selected area is too tight |
| Words split into lines | The crop is narrow or text spacing is large |
| Extra characters appear | Icons or borders are inside the crop |
| The result changes between runs | The area is too small or the screen changed |

## Fixes

- Make the selected area slightly wider and taller.
- Include the full line of text, not only the exact letters.
- Avoid cutting off shadows or outlines.
- Remove nearby icons from the selected area if they confuse the result.
- Test the same area several times.
- Use a Status Message to print the value after Read Text.

## Better Test

```text
1. Read Text from selected area into resultText
2. Status Message {resultText}
3. Stop
```

If the test reads correctly, use `resultText` in later steps or watchers.

## More About

- Read Text step: [Read Text](../Steps/Read-Text.md)
- Selected area problems: [Selected Area Problems](Selected-Area-Problems.md)
- Making areas reliable: [Making Areas Reliable](../Tips/Making-Areas-Reliable.md)
- Reading text into values: [Reading Text Into Values](../Values/Reading-Text-Into-Values.md)
- Using values later: [Using Values In Text Boxes](../Tips/Using-Values-In-Text-Boxes.md)
