# OCR Debug Captures

OCR Debug Captures saves extra files when WhirlyTask is trying to diagnose text-search problems.

Use it when Click Text is not seeing what you expect, or when you are testing text-reading behavior and need to inspect what WhirlyTask captured. Turn it back off after testing so the debug folder does not fill up.

## Where To Find It

Open:

```text
Menu > OCR Debug Captures
```

When enabled, the menu item is checked and the status says:

```text
OCR debug captures on.
```

## What It Saves

When a text search reaches a debug capture point, WhirlyTask saves:

- a `.bmp` image of the captured area
- a `.txt` report with the action, target text, area, rectangle, search mode, attempt count, image path, and OCR text result

WhirlyTask first tries to save captures beside the app:

```text
WhirlyTask folder\ocr_debug
```

If that folder cannot be created, it falls back to:

```text
%TEMP%\WhirlyTask_ocr_debug
```

## Setup

1. Turn on `Menu > OCR Debug Captures`.
2. Run the sequence or step that is failing. Click Text failures are the main case this is meant for.
3. Open the `ocr_debug` folder beside WhirlyTask, or `%TEMP%\WhirlyTask_ocr_debug`.
4. Compare the saved image and report with what you expected WhirlyTask to read.
5. Turn OCR Debug Captures off when you are done.

## What To Look For

| Debug result | What it usually means |
| --- | --- |
| The image cuts off letters | Pick a larger area |
| The image includes too much unrelated text | Pick a smaller area |
| The image is blank or wrong | The selected area or window position changed |
| The OCR text is close but not exact | Use a shorter, more stable phrase |
| The OCR text is empty | Increase the selected area or use a clearer target |

## Troubleshooting

| Problem | What to try |
| --- | --- |
| No debug files appear | Make sure OCR Debug Captures is checked before running the failing step |
| The folder is not beside WhirlyTask | Check `%TEMP%\WhirlyTask_ocr_debug` |
| Files pile up | Delete old debug files and turn the toggle off after testing |
| The capture is not useful | Re-run with the target window in the same position and state |

## More About

- Reading visible text: [Read Text](../Steps/Read-Text.md)
- Clicking visible text: [Click Text](../Steps/Click-Text.md)
- Text reading problems: [Read Text Is Wrong](../Troubleshooting/Read-Text-Is-Wrong.md)
- Selected areas: [Making Areas Reliable](../Tips/Making-Areas-Reliable.md)
