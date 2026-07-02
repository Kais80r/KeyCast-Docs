# Random Wait

Random Wait pauses for a random length of time between a minimum and maximum value.

## Fields

| Field | Meaning |
| --- | --- |
| minimum seconds | Shortest wait time |
| maximum seconds | Longest wait time |

## Setup From Scratch

1. Add Random Wait.
2. Enter the minimum seconds.
3. Enter the maximum seconds.
4. Run the sequence a few times to confirm the timing range feels right.

## Example

```text
1. Click Text Refresh
2. Random Wait 3 to 10 seconds
3. Wait For (Text) Ready timeout 30
```

## Useful For

- Optional variation in timing.
- Repeating checks without exact fixed timing.
- Spreading out repeated actions.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Testing takes too long | Use a smaller random range while building |
| The sequence waits but still fails | Use Wait For (Text), Wait For (Image), or Wait For (Window) when a real condition matters |
| The timing range is invalid | Make sure the maximum is greater than or equal to the minimum |
