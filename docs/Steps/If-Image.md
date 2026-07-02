# If Image

If Image checks whether an image target is visible, then runs the Then branch or Else branch.

Use it when the decision depends on a visual state.

## Fields

| Field | Meaning |
| --- | --- |
| Image | The image file or image target to find. Use `...` to browse for an image file. |
| Mode | `is seen` or `is not seen` |
| Area | Where to check for the image target |
| Then branch | Steps to run when the condition is true |
| Else branch | Steps to run when the condition is false |

## Setup From Scratch

1. Capture or choose a stable image target.
2. Add If Image.
3. Use `...` beside the Image field to browse for the image file, then choose the area.
4. Add a Status Message in Then.
5. Add a different Status Message in Else.
6. Test the branch.
7. Replace the test messages with real steps.

## Example

```text
If Image ready-icon is seen from selected panel area
Then:
1. Click Image ready-icon
Else:
1. Wait 1 second
2. Jump Sequence Step 1
```

## Useful For

- Visual status states.
- Icons.
- Buttons without readable text.
- Branching when text reading is unreliable.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The image condition is inconsistent | Capture a stable part of the target that does not change |
| The wrong image is matched | Use a selected area instead of a large search area |
| The condition misses an image that appears later | Use [Wait For (Image)](Wait-For.md) when you need to wait |
| Text would be more reliable | Use [If Text](If-Text.md) when the state has stable readable text |
