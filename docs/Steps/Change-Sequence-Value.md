# Change Sequence Value

Change Sequence Value changes a numeric value.

It is mainly used for counters, retry limits, loop limits, and simple state numbers.

## Fields

| Field | Meaning |
| --- | --- |
| Value name | The value to change |
| Mode | `Add`, `Subtract`, or `Set number` |
| Amount | The number to add, subtract, or set |

## Setup From Scratch

1. Create a value in Starting Values.
2. Give it a numeric starting value, such as `0`.
3. Add Change Sequence Value.
4. Choose Add, Subtract, or Set number.
5. Print it with Status Message while testing.

## Example: Count Attempts

Starting Values:

```text
attempts starts as 0
```

Main steps:

```text
1. Change Sequence Value attempts Add 1
2. Status Message Attempt {attempts}
```

## Example: Retry Limit

```text
1. Change Sequence Value attempts Add 1
2. If Sequence Value attempts >= 3
   Then:
   1. Stop Sequence
   Else:
   1. Jump Sequence Step 1
```

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The value does not change correctly | Make sure the value contains a number before using this step |
| The value goes back to its old number | Check whether [Reset and Restart Sequence](Reset-And-Restart-Sequence.md) reset it to its Starting Value |
| A counter limit is missed | Use `>=` or `<=` for limits instead of `equals` |

## More About

- Values and counters: [Values](../Values/README.md)
- Basic loop example: [Basic Loop](../Examples/Basic-Loop.md)
- Counter limit example: [Counter Limit](../Examples/Counter-Limit.md)
- Checking a counter: [If Sequence Value](If-Sequence-Value.md)
- Value watcher trigger: [When Sequence Value](../Watchers/Triggers/When-Sequence-Value.md)
