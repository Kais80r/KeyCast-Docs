# If Sequence Value

If Sequence Value checks a stored value, then runs the Then branch or Else branch.

Use it when the next steps depend on text, counters, Read Text results, or internal state.

## Fields

| Field | Meaning |
| --- | --- |
| Value name | The sequence value to check |
| Mode | `equals`, `not equals`, `contains`, `is empty`, `>`, `>=`, `<`, or `<=` |
| Compare value | Text or number to compare against |
| Then branch | Steps to run when the condition is true |
| Else branch | Steps to run when the condition is false |

## Setup From Scratch

1. Create the value in Starting Values.
2. Fill it with Set Sequence Value, Change Sequence Value, or Read Text.
3. Add If Sequence Value.
4. Choose the comparison mode.
5. Add steps inside Then and Else.
6. Add Status Message inside both branches while testing.

## Example: Check Read Text

```text
1. Read Text statusText from selected status area
2. If Sequence Value statusText contains Complete
   Then:
   1. Status Message Finished
   Else:
   1. Wait 2 seconds
   2. Jump Sequence Step 1
```

## Example: Check Counter

```text
1. Change Sequence Value attempts Add 1
2. If Sequence Value attempts >= 5
   Then:
   1. Stop Sequence
   Else:
   1. Jump Sequence Step 1
```

## Choosing A Mode

| Mode | Use when |
| --- | --- |
| equals | The value must match exactly |
| not equals | Anything except the compare value should pass |
| contains | The value may include extra text or line breaks |
| is empty | The value should be blank |
| `>`, `>=`, `<`, `<=` | The value is a clean number |

## Troubleshooting

| Problem | What to try |
| --- | --- |
| OCR text does not match exactly | Use `contains` when the value may include spaces, line breaks, or small OCR changes |
| Number comparison does not work | Make sure the value contains only the number you want to compare |
| The branch uses an empty value | Fill the value before this If step runs |

## More About

- Values: [Values](../Values/README.md)
- Reading text into values: [Reading Text Into Values](../Values/Reading-Text-Into-Values.md)
- Read Text step: [Read Text](Read-Text.md)
- Value placeholders in text boxes: [Using Values In Text Boxes](../Tips/Using-Values-In-Text-Boxes.md)
- Value watcher trigger: [When Sequence Value](../Watchers/Triggers/When-Sequence-Value.md)
- Blank value troubleshooting: [Value Is Blank](../Troubleshooting/Value-Is-Blank.md)
