# Note

Note leaves a reminder in the step list.

It is useful for labeling sections or explaining why nearby steps are there.

## Fields

| Field | Meaning |
| --- | --- |
| Note text | The explanation shown in the editor |

## When To Use It

Use notes to explain why a section exists, especially in long sequences.

## Example

```text
1. Note: This section waits for the report to finish
2. Click Text Generate
3. Wait For (Text) Complete timeout 60
```

## Useful For

- Marking sections.
- Explaining watcher recovery logic.
- Explaining why a jump goes to a specific step.
- Leaving reminders for future edits.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Nothing appears during playback | Use [Status Message](Status-Message.md) when you need a visible message |
| The note is hard to understand later | Write what the nearby steps are for, not just `fix` or `thing` |
| The note mentions old step numbers | Update notes after moving or deleting steps |
