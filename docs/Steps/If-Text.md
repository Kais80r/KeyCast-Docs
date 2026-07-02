# If Text

If Text checks whether specific text is visible, then runs the Then branch or Else branch.

Use it when the workflow should choose a path based on what the screen currently shows.

## Fields

| Field | Meaning |
| --- | --- |
| Text | The text to search for |
| Mode | `is seen` or `is not seen` |
| Area | Where to check for the text |
| Then branch | Steps to run when the condition is true |
| Else branch | Steps to run when the condition is false |

## Setup From Scratch

1. Add If Text.
2. Enter the text to check.
3. Choose the area.
4. Add a Status Message in the Then branch.
5. Add a different Status Message in the Else branch.
6. Run once to confirm the correct branch runs.
7. Replace the test messages with real steps.

## Example

```text
If Text Complete is seen from selected status area
Then:
1. Status Message Complete
Else:
1. Wait 1 second
2. Jump Sequence Step 1
```

## When To Use Wait For (Text) Instead

Use [Wait For (Text)](Wait-For.md) when the sequence should pause until the text appears.

Use If Text when the sequence should choose between two paths right now.

## Useful For

- Skipping work when something is already done.
- Choosing a recovery path.
- Checking if a warning is visible.
- Branching based on a current screen state.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Branch testing is confusing | Start each branch with a simple Status Message before adding real actions |
| The wrong copy of text is detected | Use a selected area around the correct part of the screen |
| `is not seen` passes too easily | Test the selected area with the text visible before trusting the negative check |
| The text appears later | Use [Wait For (Text)](Wait-For.md) when you need to wait |
