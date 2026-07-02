# Open App/File

Open App/File opens a program, file, folder, or target path immediately.

## Fields

| Field | Meaning |
| --- | --- |
| Target | App name, file path, folder path, or other openable target |

## Setup From Scratch

1. Add Open App/File.
2. Enter the target.

## Example

```text
1. Open App/File C:\Reports\summary.xlsx
```

Example with follow-up input:

```text
1. Open App/File C:\Reports\summary.xlsx
2. Wait For (Window) summary is open timeout 30
3. Focus Window summary
```

## Useful For

- Opening apps.
- Opening files.
- Opening folders.
- Starting a workflow from a known target.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The app or file does not open | Use the full path when the target is not found reliably |
| The next step runs too early | Add [Wait For (Window)](Wait-For.md) or [Wait For (Text)](Wait-For.md) after opening |
| The target is a website | Use [Open Link](Open-Link.md) for web links |
