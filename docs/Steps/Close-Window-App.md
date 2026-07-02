# Close Window/App

Close Window/App sends a close request to a matching window or app by title.

## Fields

| Field | Meaning |
| --- | --- |
| Window title | Text that appears in the window title |

## Setup From Scratch

1. Add Close Window/App.
2. Enter a stable title fragment.

## Example

```text
1. Close Window/App Temporary Report
```

Example with confirmation:

```text
1. Close Window/App Temporary Report
2. Wait For (Window) Temporary Report is not open timeout 10
```

## Useful For

- Cleaning up temporary windows.
- Closing dialogs or tools after a workflow.
- Returning the desktop to a known state.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The wrong window closes | Use a more specific title fragment |
| Unsaved work could be lost | Save or confirm the target state before closing the window |
| A confirmation prompt appears | Add steps after closing to handle the prompt safely |
