# Take Screenshot

Take Screenshot captures the screen area you choose and saves it as a `.bmp` image.

Screenshots are saved in the WhirlyTask screenshots folder:

```text
%LOCALAPPDATA%\WhirlyTask\screenshots
```

## Fields

| Field | Meaning |
| --- | --- |
| Area | The screen area to capture |
| name | Optional filename prefix |

## What It Actually Does

When playback reaches this step, WhirlyTask captures the selected area at its real size and writes a bitmap file.

The filename uses the name field, a timestamp, and the current WhirlyTask process id. For example:

```text
screenshot_20260629-211538-042_12345.bmp
```

If the name field is empty, WhirlyTask uses `screenshot` as the prefix. Characters that Windows cannot use in a filename are replaced with `_`.

## Setup From Scratch

1. Add Take Screenshot.
2. Choose Full Screen for a first test, or choose Pick Area to select a specific part of the screen.
3. Optionally set the name field, such as `before-click` or `result`.
4. Run the sequence.
5. Open the WhirlyTask screenshots folder in `%LOCALAPPDATA%\WhirlyTask\screenshots`.

## Example: Capture The Whole Screen

```text
1. Take Screenshot Full Screen name screenshot
2. Status Message Screenshot saved
```

## Example: Capture A Result Area

```text
1. Wait For (Text) Complete timeout 30 sec
2. Take Screenshot selected result area name result
3. Status Message Result screenshot saved
```

## Values

The name field can use sequence values:

```text
result-{runNumber}
```

This is useful when a sequence saves multiple screenshots and each one should have a meaningful prefix.

## Area Tips

- Use Full Screen when you need the whole desktop.
- Use Pick Area when you only need one panel, message, score, or result.
- Leave a little margin around the thing you want to capture.
- If the target window moves between runs, focus or fullscreen the window before the screenshot step.

## Useful For

- Saving proof that a sequence reached a result screen.
- Capturing an error or recovery state from a watcher.
- Recording before-and-after states during testing.
- Saving an area before a click, restart, or app close step changes it.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| No screenshot appears | Check `%LOCALAPPDATA%\WhirlyTask\screenshots` |
| Screenshot save failed | Make sure the screenshots folder can be created and written to |
| The wrong area is captured | Pick the area again, or use Full Screen for a test |
| The filename is not exactly what you typed | Windows-invalid filename characters are replaced with `_` |

## More About

- Selecting areas for screen steps: [Selected Area Problems](../Troubleshooting/Selected-Area-Problems.md)
- Reading text from an area: [Read Text](Read-Text.md)
- Waiting before a capture: [Wait For (Text)](Wait-For.md)
- Showing progress after a capture: [Status Message](Status-Message.md)
