# If Window

If Window checks a window condition, then runs the Then branch or Else branch.

## Fields

| Field | Meaning |
| --- | --- |
| Window title | Text that appears in the window title |
| Mode | `is open`, `is not open`, `is focused`, `is not focused`, `is fullscreen`, or `is not fullscreen` |
| Then branch | Steps to run when the condition is true |
| Else branch | Steps to run when the condition is false |

## Setup From Scratch

1. Add If Window.
2. Enter a stable part of the window title.
3. Choose the mode.
4. Add Status Message in Then and Else to test.
5. Replace the messages with real actions after the branch works.

## Example

```text
If Window Report Tool is focused
Then:
1. Press Key Ctrl+S
Else:
1. Focus Window Report Tool
2. Press Key Ctrl+S
```

## When To Use Wait For (Window) Instead

Use [Wait For (Window)](Wait-For.md) when the sequence should pause until the condition happens.

Use If Window when the sequence should choose between two paths right now.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The branch runs while another window is active | Check `is focused` instead of only `is open` |
| The wrong window matches | Use a more specific title fragment |
| The window appears later | Use [Wait For (Window)](Wait-For.md) when you need to wait |
