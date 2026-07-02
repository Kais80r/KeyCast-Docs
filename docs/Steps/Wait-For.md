# Wait For

Wait For pauses the sequence until one chosen condition becomes true, or until the timeout runs out.

Use the Type field to choose what the step waits for:

- `Text`
- `Image`
- `Window`
- `Internet`

This replaces the older separate wait-for step choices for Text, Image, Window, and Internet.

## Fields

| Field | Meaning |
| --- | --- |
| Type | What kind of condition to wait for: Text, Image, Window, or Internet |
| Text/Image/Window | The target to look for when the selected type needs one |
| Area | Where to search for text or image targets |
| Mode | The condition that must become true |
| timeout | Maximum seconds to wait before the step gives up |

## Modes By Type

| Type | Modes |
| --- | --- |
| Text | `is seen`, `is not seen` |
| Image | `is seen`, `is not seen` |
| Window | `is open`, `is not open`, `is focused`, `is not focused`, `is fullscreen`, `is not fullscreen` |
| Internet | `is online`, `is offline` |

## Setup From Scratch

1. Add the action that should make something appear, disappear, open, close, or connect.
2. Add Wait For after it.
3. Choose the Type.
4. Fill in the target fields for that type.
5. Choose the mode.
6. Set a timeout so the sequence cannot wait forever.

## Example: Wait For (Text)

```text
1. Click Text Submit
2. Wait For (Text) Complete from selected status area timeout 30
3. Status Message Finished
```

## Example: Wait For (Image)

```text
1. Click Text Start
2. Wait For (Image) ready-icon from selected panel area timeout 30
3. Click Image ready-icon
```

## Example: Wait For (Window)

```text
1. Open App/File report-tool.exe
2. Wait For (Window) Report Tool is open timeout 30
3. Focus Window Report Tool
```

## Example: Wait For (Internet)

```text
1. Wait For (Internet) is online timeout 60
2. Open Link https://example.com
```

## Useful For

- Replacing guessed delays with real readiness checks.
- Waiting for loading text or icons to disappear.
- Waiting for apps or dialogs to open or close.
- Pausing network-dependent steps until the connection state is right.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The wait times out | Increase the timeout or make the target/mode more specific |
| Text or image matches the wrong place | Use a selected area around the expected location |
| Window matching finds the wrong window | Use a more specific title fragment |
| Internet is online but a page is still loading | Follow Wait For (Internet) with Wait For (Text) or Wait For (Image) readiness checks |

## More About

- Clicking text after it appears: [Click Text](Click-Text.md)
- Clicking an image after it appears: [Click Image](Click-Image.md)
- Text conditions: [If Text](If-Text.md)
- Image conditions: [If Image](If-Image.md)
- Window conditions: [If Window](If-Window.md)
- Internet conditions: [If Internet](If-Internet.md)
- Reliable selected areas: [Making Areas Reliable](../Tips/Making-Areas-Reliable.md)