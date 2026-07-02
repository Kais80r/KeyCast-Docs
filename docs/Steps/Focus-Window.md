# Focus Window

Focus Window restores a matching window and brings it to the front.

## Fields

| Field | Meaning |
| --- | --- |
| Window title | Text that appears in the window title |

## Setup From Scratch

1. Add Focus Window.
2. Enter a stable part of the title.

## Example

```text
1. Focus Window Report Tool
2. Press Key Ctrl+S
```

Example with readiness checks:

```text
1. Wait For (Window) Report Tool is open timeout 30
2. Focus Window Report Tool
3. Wait 0.5 seconds
4. Press Key Ctrl+S
```

## Useful For

- Preparing for keyboard input.
- Preparing for Play Track.
- Returning focus after another window interrupted the workflow.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The wrong window is focused | Use a more specific title fragment |
| Keys go missing after focus | Add a short wait before pressing keys |
| The window is focused but not ready | Follow this step with [Wait For (Text)](Wait-For.md) or [Wait For (Window)](Wait-For.md) |

## More About

- Waiting for a window: [Wait For (Window)](Wait-For.md)
- Fullscreening a window: [Fullscreen Window](Fullscreen-Window.md)
- Keyboard input after focus: [Press Key](Press-Key.md)
- Focus troubleshooting: [Wrong Window Or Focus](../Troubleshooting/Wrong-Window-Or-Focus.md)
