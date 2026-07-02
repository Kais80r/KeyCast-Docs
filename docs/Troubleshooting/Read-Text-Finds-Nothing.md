# Read Text Finds Nothing

This page is for cases where Read Text returns an empty value.

## Check These First

- The selected area actually covers the text.
- The text is not covered by another window.
- The text is visible at the moment the step runs.
- The selected area is not too small.
- The value name exists in Starting Values.
- The step stores text into the value you expect.

## Common Fixes

- Add a Wait step before Read Text.
- Try Full Screen once to confirm the text can be read.
- Make the selected area larger.
- Use a Status Message after Read Text.
- Make sure the window is active and not minimized.

## Test Pattern

```text
1. Wait 1 second
2. Read Text from Full Screen into resultText
3. Status Message {resultText}
4. Stop
```

If Full Screen works but the selected area does not, the issue is the selected area.
