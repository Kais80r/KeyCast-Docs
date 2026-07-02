# For Chance

For Chance randomly chooses whether to run the Then branch or Else branch.

## Fields

| Field | Meaning |
| --- | --- |
| percent | Chance that the Then branch runs |
| Then branch | Steps to run when the chance succeeds |
| Else branch | Steps to run when the chance fails |

## Setup From Scratch

1. Add For Chance.
2. Enter a percent, such as `25` or `50`.
3. Add Status Message in Then and Else while testing.
4. Replace the messages with the real optional behavior.

## Example

```text
For Chance 25
Then:
1. Status Message Optional check ran
Else:
1. Status Message Optional check skipped
```

## Useful For

- Optional behavior.
- Occasional checks.
- Testing branch behavior without forcing it every run.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Important recovery is unreliable | Use a real condition such as If Text, If Image, or If Window |
| Testing feels unpredictable | Temporarily use a fixed branch while testing, then restore the chance value |
| The percent is unclear | Use a simple value like `10`, `25`, `50`, or `75` |
