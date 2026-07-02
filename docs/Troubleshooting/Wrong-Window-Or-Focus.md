# Wrong Window Or Focus

This page is for key presses, mouse clicks, or recorded tracks going to the wrong app or window.

## Why It Happens

Keyboard and mouse steps act on the currently active window. If another window has focus, input can go there instead.

## Fixes

- Click or activate the correct window before pressing keys.
- Add a short Wait after opening windows.
- Use Wait Until Window if the window needs time to appear.
- Use Click Text or Click Image when the target can move.
- Add a watcher for unexpected windows.

## Test Pattern

```text
1. Wait Until Window target window
2. Click Text field name
3. Press key Enter
```
