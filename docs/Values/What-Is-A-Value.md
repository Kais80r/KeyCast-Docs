# What Is A Value

A value is a named piece of text stored inside a sequence.

It can start with text, stay empty, or be changed while the sequence runs.

Values are how one step passes information to another step.

## Why Values Matter

Values let steps share information.

Example:

```text
1. Read Text into statusText
2. If Value statusText contains Complete
3. Status Message Done: {statusText}
```

The Read Text step fills the value. The If Value step checks it. The Status Message step displays it.

## Starting Values

Starting Values define what a value contains when the sequence begins.

Examples:

```text
statusText starts as empty
attempts starts as 0
isReady starts as false
```

If the sequence uses Reset and Restart Sequence, values return to these starting values.

## Values Are Text

Even numbers are stored as text first. Number comparisons only work well when the value contains a clean number.

If a value contains extra symbols or words, use `contains` instead of a number comparison.

## Placeholders

Use braces to insert a value into a text box:

```text
Current result: {resultText}
Attempt: {attempts}
```

When the step runs, WhirlyTask replaces the placeholder with the current value.

If the value name is `ResultText`, the placeholder must be `{ResultText}`. Spelling and capitalization matter.

## Common Value Patterns

| Pattern | Example |
| --- | --- |
| Store screen text | Read Text fills `statusText` |
| Count loops | Change Sequence Value adds 1 to `loops` |
| Store state | Set Sequence Value sets `state` to `waiting` |
| Send a result | Discord Message sends `Result: {resultText}` |
| Trigger a watcher | Watcher fires when `state` changed |

## More About

- [Values](README.md)
- [Using Values In Messages](Using-Values-In-Messages.md)
- [Reading Text Into Values](Reading-Text-Into-Values.md)
- [Using Values In Text Boxes](../Tips/Using-Values-In-Text-Boxes.md)
