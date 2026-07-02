# When Sequence Value

Use When Sequence Value when a watcher should react to a value stored inside the sequence.

Values are named text fields. They can be set manually, changed by steps, or filled by Read Text.

This trigger is useful when the important change is inside WhirlyTask, not directly on the screen.

## Common Conditions

| Condition | Meaning |
| --- | --- |
| contains | The value includes the text |
| equals | The value matches exactly |
| bigger than | The value is treated like a number and compared |
| smaller than | The value is treated like a number and compared |
| changed | The value is different from its previous value |

## Important: Changed

`changed` means the value became different while the sequence was running.

Example:

```text
Starting value:
status starts as Waiting

Watcher:
When Sequence Value status changed
```

This watcher fires after a step changes `status` to something else.

## Setup Example

```text
Starting value:
resultText starts as empty

Main step:
Read Text into resultText

Watcher trigger:
When Sequence Value resultText contains Complete
```

## Common Uses

| Need | Condition |
| --- | --- |
| Stop when a counter reaches a limit | `loops >= 30` |
| React when Read Text finds a phrase | `resultText contains Complete` |
| React when a state changes | `state changed` |
| Detect a specific state | `state equals waiting` |

## When Changed Is Useful

Use `changed` when any new value should trigger the watcher.

Example:

```text
Main steps:
1. Read Text statusText

Watcher:
When Sequence Value statusText changed
1. Status Message New status: {statusText}
```

If you need a specific result, use `contains` or `equals` instead.

## Tips

- Print the value with Status Message: `{resultText}`.
- Check spelling. `statusText` and `statustext` are different names.
- For number comparisons, make sure the value only contains a number.
- Use `contains` when the value may include extra words or line breaks.

## More About

- [Values](../../Values/README.md)
- [If Sequence Value](../../Steps/If-Sequence-Value.md)
- [Counter Limit](../../Examples/Counter-Limit.md)
- [Value Is Blank](../../Troubleshooting/Value-Is-Blank.md)
