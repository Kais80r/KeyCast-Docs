# Run Advanced Track

Run Advanced Track runs a saved advanced track from inside a sequence.

Advanced tracks are useful for reusable action blocks that are more structured than a normal recorded track.

If you are not sure what an advanced track is, read [Advanced Track](../Basics/Advanced-Track.md) first.

## Fields

| Field | Meaning |
| --- | --- |
| Advanced track | The saved advanced track to run |
| Repeat | How many times to run it |

## Setup From Scratch

1. Create and save an advanced track.
2. Add Run Advanced Track to a sequence.
3. Choose the saved advanced track.
4. Set Repeat.

## Example

```text
1. Run Advanced Track Fill Form repeat 1
```

Example with a result check:

```text
1. Run Advanced Track Fill Form repeat 1
2. Wait For (Text) Complete timeout 30
3. Status Message Form finished
```

## Useful For

- Reusing a longer action list.
- Sharing common setup steps across sequences.
- Keeping the main sequence readable.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The advanced track needs recovery logic | Put watcher-style recovery in the sequence that runs the advanced track |
| The advanced track should exit early | Use [Return to Sequence](Return-To-Sequence.md) inside the advanced track |
| The wrong app state is active | Focus or wait for the correct app/window before running the advanced track |

Related basics: [Choosing What To Use](../Basics/Choosing-What-To-Use.md)
