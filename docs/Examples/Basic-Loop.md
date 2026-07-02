# Basic Loop

Use this pattern when a group of steps should repeat.

For a known number of repeats, use [Repeat X Times](../Steps/Repeat-X-Times.md). For an open-ended loop, use a jump step with a clear stop condition.

## Repeat A Fixed Number Of Times

```text
1. Repeat 5 times
   1. Do the repeated action
   2. Wait 1 second
2. Status Message Finished
```

Replace `Do the repeated action` with real steps, such as Play Track, Run Advanced Track, Click Text, or Read Text.

## Open-Ended Loop

```text
1. Do the repeated action
2. Wait 1 second
3. Jump Sequence Step 1
```

This loops forever until the sequence is stopped or another step branches away.

## Why These Work

- `Repeat X Times` is easiest when the repeat count is known.
- `Jump Sequence Step` is useful when the sequence needs to return to an earlier main step.
- `Wait` gives the target app time before the loop repeats.

## When To Add A Stop Limit

Give the loop a safety limit when:

- The loop could run forever by accident.
- The target app might never reach the expected state.
- You only want a maximum number of attempts.
- You are testing and want a built-in stop path in addition to the Stop hotkey.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The repeat runs too many times | Check the number in Repeat X Times |
| The jump loop jumps to the wrong place | Recheck jump targets after editing the step list |
| The loop never stops | Add a counter, condition, or Stop Sequence path |
| Values reset unexpectedly | Use Jump Sequence Step instead of Reset and Restart Sequence when values should be kept |

## Add A Stop Limit

If the loop should stop after a number of runs, use [Counter Limit](Counter-Limit.md).

## More About

- Fixed repeat blocks: [Repeat X Times](../Steps/Repeat-X-Times.md)
- Looping back to an earlier step: [Jump Sequence Step](../Steps/Jump-Sequence-Step.md)
- Adding a stop limit: [Counter Limit](Counter-Limit.md)
- Waiting between repeats: [Wait](../Steps/Wait.md)
- Waiting for real screen state: [Wait For](../Steps/Wait-For.md)
- Building reliable sequences: [Build A Reliable Sequence](../Guides/Build-A-Reliable-Sequence.md)