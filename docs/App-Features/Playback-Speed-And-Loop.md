# Playback, Speed, And Loop

Playback settings decide how a loaded item runs.

## Playback Speed

Speed changes how fast recorded playback runs.

Higher speed makes playback faster. Lower speed makes playback slower.

Use slower playback when:

- The target app is slow.
- Recorded actions happen too quickly.
- You are debugging a track.

Use faster playback when:

- The target app responds quickly.
- The track has unnecessary delays.

## Loop Playback

Loop playback repeats a loaded track.

There are two loop controls:

- the Loop button on the main window
- `Menu > Continuous Playback`

Loop only works for tracks. If a sequence needs looping, build the loop inside the sequence with steps like [Jump Sequence Step](../Steps/Jump-Sequence-Step.md) and counters.

## Loop Count

The loop count decides how many times the track repeats.

Example:

```text
Loop enabled
Loop count: 5
```

The loaded track plays five times.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Loop is disabled | Load a track. Sequences need loop steps inside the sequence |
| The loop repeats too fast | Lower playback speed or add waits between repeated actions |
| A sequence does not loop | Use [Jump Sequence Step](../Steps/Jump-Sequence-Step.md) or the [Basic Loop](../Examples/Basic-Loop.md) pattern |
| The target app is not ready between repeats | Add waits or wait-for checks before the next repeat |

## Tips

- For track repetition, use Loop.
- For sequence repetition, use [Basic Loop](../Examples/Basic-Loop.md).
- Add waits or wait-for checks between repeated actions when the app needs time.
