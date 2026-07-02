# Screen Text Reading Workflow

This guide explains how to read visible text from the screen and use it in a sequence.

The technical word for screen text reading is OCR. The important idea is simple: WhirlyTask looks at part of the screen, detects letters, and stores the result in a value.

## When To Use Screen Text Reading

Use it when visible text should affect what the automation does.

Examples:

- Read a status label.
- Read a result message.
- Read a number that changes.
- Send visible text in a Discord message.
- Let a watcher react when newly read text changes.

## Basic Pattern

```text
Starting Values:
resultText starts as empty

Main Steps:
1. Read Text resultText from selected area
2. Status Message Read: {resultText}
3. If Sequence Value resultText contains Complete
```

The Read Text step stores the detected text in `resultText`.

## Setup From Scratch

1. Add a Starting Value, for example `resultText`.
2. Leave the starting value empty unless you need a default.
3. Add [Read Text](../Steps/Read-Text.md).
4. Choose `resultText` as the destination value.
5. Start with Full Screen or a generous selected area.
6. Add [Status Message](../Steps/Status-Message.md) with `Read: {resultText}`.
7. Run the sequence.
8. Narrow the area only after the text reads correctly.

## Choosing The Area

The selected area should include the whole text and a little space around it.

Good area:

```text
[ small margin ][ full text ][ small margin ]
```

Risky area:

```text
[letters cut close to the edges]
```

Small areas can fail because the reading engine has less context. Colored text, outlines, shadows, icons, and cropped punctuation can make this worse.

More detail: [Making Areas Reliable](../Tips/Making-Areas-Reliable.md)

## Use The Text Later

After text is in a value, other steps can use it.

| Need | Example |
| --- | --- |
| Show it inside WhirlyTask | `Status Message Read: {resultText}` |
| Send it to Discord | `Discord Message Result: {resultText}` |
| Branch based on it | `If Sequence Value resultText contains Complete` |
| Watch for changes | `When Sequence Value resultText changed` |

## Choosing Contains Or Equals

Use `contains` most of the time.

Screen text reading may include line breaks, extra spaces, or small mistakes. `equals` only works well when the detected text is very stable.

Example:

```text
Better:
resultText contains Complete

Riskier:
resultText equals Complete
```

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Text is blank | Use Full Screen once, then select the area again |
| Text is partly wrong | Make the area larger and avoid cutting letters |
| Icons become letters | Select the text without nearby icons if possible |
| The message shows `{resultText}` literally | Check the value name and braces |
| The branch does not run | Print the value with Status Message and compare what it actually contains |

## More About

- [Read Text](../Steps/Read-Text.md)
- [Reading Text Into Values](../Values/Reading-Text-Into-Values.md)
- [Read Text Is Wrong](../Troubleshooting/Read-Text-Is-Wrong.md)
- [Read Text Finds Nothing](../Troubleshooting/Read-Text-Finds-Nothing.md)
- [Selected Area Problems](../Troubleshooting/Selected-Area-Problems.md)
