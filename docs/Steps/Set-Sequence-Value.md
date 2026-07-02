# Set Sequence Value

Set Sequence Value replaces a stored value with new text.

Values are how a sequence remembers information. Other steps can read those values later by using `{ValueName}`.

## Fields

| Field | Meaning |
| --- | --- |
| Value name | The value to change |
| Value | The text or number to store |

## Setup From Scratch

1. Add the value in Starting Values.
2. Add Set Sequence Value.
3. Choose the same value name.
4. Enter the text or number to store.
5. Add Status Message to test it.

## Example: Store Text

Starting Values:

```text
state starts as empty
```

Main steps:

```text
1. Set Sequence Value state to Waiting
2. Status Message State: {state}
```

## Example: Reset A Counter

```text
1. Set Sequence Value attempts to 0
2. Status Message Attempts reset: {attempts}
```

## What You Can Store

- Plain text.
- Numbers.
- Text that includes other values.
- Temporary state like `ready`, `waiting`, or `failed`.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The value is not found | Create it in Starting Values first |
| The wrong value is changed | Match the value name exactly, including capitalization |
| A counter should increase or decrease | Use [Change Sequence Value](Change-Sequence-Value.md) instead |

## More About

- Values: [Values](../Values/README.md)
- Using values in text boxes: [Using Values In Text Boxes](../Tips/Using-Values-In-Text-Boxes.md)
- Changing numeric values: [Change Sequence Value](Change-Sequence-Value.md)
- Checking a value: [If Sequence Value](If-Sequence-Value.md)
- Blank value troubleshooting: [Value Is Blank](../Troubleshooting/Value-Is-Blank.md)
