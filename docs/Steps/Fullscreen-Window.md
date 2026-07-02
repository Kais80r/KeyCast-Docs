# Fullscreen Window

Fullscreen Window finds a matching window by title, brings it forward, and maximizes it.

## Fields

| Field | Meaning |
| --- | --- |
| Window title | Text that appears in the window title |

## Setup From Scratch

1. Add Fullscreen Window.
2. Enter a stable part of the title.

## Example

```text
1. Fullscreen Window Report Tool
```

Example before screen reading:

```text
1. Fullscreen Window Report Tool
2. Wait 1 second
3. Read Text statusText from selected status area
```

## Useful For

- Making selected areas more consistent.
- Stabilizing screen layout before image or text checks.
- Preparing a window for recorded tracks.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Selected areas no longer line up | Fullscreen the window before choosing OCR or image areas |
| The wrong window changes size | Use a more specific title fragment |
| The app does not enter fullscreen | Test the app manually and use [Focus Window](Focus-Window.md) or normal window sizing if needed |
