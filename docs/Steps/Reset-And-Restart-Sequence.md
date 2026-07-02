# Reset and Restart Sequence

Reset and Restart Sequence resets values and starts the current sequence over from the beginning.

It also resets every sequence value back to its Starting Value.

That means:

- Values filled by Read Text are cleared back to their starting text.
- Counters changed with Change Sequence Value go back to their starting number.
- Values changed with Set Sequence Value go back to their starting text.

## Fields

This step has no fields.

## Setup From Scratch

1. Add Reset and Restart Sequence after a recovery action.
2. Make sure restarting the workflow is safe.
3. Check whether resetting all values to their Starting Values is what you want.

## Example

```text
Watcher steps:
1. Pause Sequence
2. Click Text Reset
3. Reset and Restart Sequence
```

## Useful For

- Starting over after recovery.
- Returning to a known starting state.
- Repeating a workflow from its Starting Values.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| A counter should keep increasing | Use [Jump Sequence Step](Jump-Sequence-Step.md) instead of resetting the sequence |
| The sequence restarts forever | Add a counter, condition, or Stop Sequence path |
| Values lose their current contents | Remember that every value returns to its Starting Value |

## More About

- [Values](../Values/README.md)
- [Pause Sequence](Pause-Sequence.md)
- [Watcher Recovery Workflow](../Guides/Watcher-Recovery-Workflow.md)
- [Counter Limit](../Examples/Counter-Limit.md)
