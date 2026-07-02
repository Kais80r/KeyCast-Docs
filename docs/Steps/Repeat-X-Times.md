# Repeat X Times

Repeat X Times runs a nested group of steps a fixed number of times, then continues with the next step after the repeat block.

Use this when you already know how many times something should happen.

## Fields

| Field | Meaning |
| --- | --- |
| times | How many times to run the nested steps |
| Steps | The content that repeats |

## Setup From Scratch

1. Add Repeat X Times.
2. Enter the number of times to repeat.
3. Use `+ Add Step` inside the repeat block.
4. Add the steps that should run each time.
5. Add any steps that should happen after the repeat block below it.

## Example: Press A Key Five Times

```text
1. Repeat 5 times
   1. Press Key E hold 0.05 sec
   2. Wait 0.2 seconds
2. Status Message Done
```

## Example: Try A Button Three Times

```text
1. Repeat 3 times
   1. Click Text Retry
   2. Wait For (Text) Loading is not seen timeout 10
2. Status Message Retry block finished
```

## How It Behaves

Repeat X Times checks the count before it starts. If the count is `3`, the nested steps run three full times.

A nested Stop Sequence, Reset and Restart Sequence, Return to Sequence, or jump step can still interrupt the repeat block.

## Useful For

- Pressing or clicking a fixed number of times.
- Trying a short action several times.
- Running a small reusable block without building a jump loop.
- Keeping simple loops easier to read.

## Common Mistakes

| Problem | What to try |
| --- | --- |
| The block runs too many times | Check the number in the times field |
| The sequence continues too early | Put all repeated steps inside the Repeat X Times block |
| You need to stop based on screen state | Use an If step or watcher pattern, not only a fixed repeat count |
| You need an endless loop | Use a jump loop or sequence loop pattern instead |

## More About

- Fixed waits between repeats: [Wait](Wait.md)
- Branching during a repeat: [If Text](If-Text.md)
- Looping to an earlier step: [Jump Sequence Step](Jump-Sequence-Step.md)
- Basic loop pattern: [Basic Loop](../Examples/Basic-Loop.md)