# Jump Block Step

Jump Block Step jumps to another step inside the current block.

## Fields

| Field | Meaning |
| --- | --- |
| Step number | The target step number in the current block |

## What A Block Means

A block is the step list you are currently inside.

Examples of blocks:

- Main steps.
- Watcher steps.
- Then branch.
- Else branch.

## Setup From Scratch

1. Decide which local step should run next.
2. Add Jump Block Step.
3. Enter that step number.
4. Add Status Message while testing so you can see the loop or jump.

## Example: Local Loop

```text
1. Change Sequence Value attempts Add 1
2. If Sequence Value attempts < 3
   Then:
   1. Jump Block Step 1
   Else:
   1. Stop Sequence
```

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The jump goes to the wrong place | Check that the target step number is inside the same branch block |
| You need to jump from a watcher to the main sequence | Use [Jump Sequence Step](Jump-Sequence-Step.md) instead |
| The target changed after editing | Recheck jump targets after inserting, deleting, or moving steps |

## More About

- Basic loop example: [Basic Loop](../Examples/Basic-Loop.md)
- Jumping in the main sequence: [Jump Sequence Step](Jump-Sequence-Step.md)
- Jumping inside a watcher: [Jump to Watcher Step](Jump-To-Watcher-Step.md)
- Branching with values: [If Sequence Value](If-Sequence-Value.md)
