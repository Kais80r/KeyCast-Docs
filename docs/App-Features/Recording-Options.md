# Recording Options

Recording options decide what WhirlyTask records into tracks.

They affect new recordings. Old saved tracks keep their existing recorded input.

## Where To Find Them

Open:

```text
Menu > Recording
```

## Options

| Option | Meaning |
| --- | --- |
| Record Mouse Movement | Records mouse movement between actions |
| Record Mouse Buttons/Wheel | Records clicks, releases, wheel, and horizontal wheel |
| Record Mouse Positions | Stores positions for mouse actions |
| Record Keyboard | Records keyboard key presses |

## When To Turn Things Off

Turn off mouse movement when:

- Tracks contain too much noisy movement.
- Only clicks matter.
- You want cleaner recordings.

Turn off mouse positions when:

- You want mouse button actions without fixed screen positions.
- You are testing keyboard-only workflows.

Turn off keyboard when:

- You only want mouse actions.
- You are using the keyboard while recording but only want mouse actions saved.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The recording has too much mouse movement | Turn off `Record Mouse Movement` before recording again |
| Clicks replay in the wrong place | Turn off fixed mouse positions when possible, or use [Click Text](../Steps/Click-Text.md) or [Click Image](../Steps/Click-Image.md) |
| Keys are missing | Turn on `Record Keyboard` before recording |
| Mouse clicks are missing | Turn on `Record Mouse Buttons/Wheel` before recording |

## Tips

- For stable UI positions, recording positions can be useful.
- For moving UI, use sequences with [Click Text](../Steps/Click-Text.md) or [Click Image](../Steps/Click-Image.md).
- Keep tracks short and clean.
