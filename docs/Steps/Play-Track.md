# Play Track

Play Track runs one of your saved tracks inside the current sequence.

A track is useful for replaying keyboard and mouse input that you already recorded.

If you are not sure what a track is, read [Track](../Basics/Track.md) first.

## Fields

| Field | Meaning |
| --- | --- |
| Track | The saved track to run |
| Repeat | How many times to run it |

## Setup From Scratch

1. Record and save a track in WhirlyTask.
2. Open the sequence editor.
3. Add Play Track.
4. Choose the saved track.
5. Set Repeat.

## Example

```text
1. Play Track Fill Date Fields repeat 1
```

Example with app readiness checks:

```text
1. Focus Window Report Tool
2. Play Track Fill Date Fields repeat 1
3. Wait For (Text) Ready timeout 30
```

## Useful For

- Reusing recorded input.
- Keeping sequences shorter.
- Repeating a stable interaction.
- Combining recorded actions with conditions and watchers.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The track plays into the wrong app | Use [Focus Window](Focus-Window.md) before Play Track |
| The track is hard to reuse | Split large recordings into shorter tracks |
| The next step runs too early | Add a wait or wait-for step after playback |
| Clicks fail when the UI moves | Use [Click Text](Click-Text.md) or [Click Image](Click-Image.md) for moving targets |

Related basics: [Choosing What To Use](../Basics/Choosing-What-To-Use.md)
