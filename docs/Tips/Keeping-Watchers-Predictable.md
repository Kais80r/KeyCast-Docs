# Keeping Watchers Predictable

Watchers are powerful because they run in the background. That also means they should be kept simple.

## Give Each Watcher One Job

Good watcher jobs:

- Stop when a counter reaches a limit.
- Handle one warning popup.
- Send one notification when important text appears.
- Reset and restart when a connection problem appears.

Avoid making one watcher handle many unrelated problems.

## Use Cooldowns

A cooldown prevents the same watcher from firing repeatedly too fast.

Use a longer cooldown for alerts and messages. Use a shorter cooldown only when the watcher must react quickly.

## Decide If It Should Take Over

If the watcher only sends a message or stops the sequence, it may not need Pause Sequence.

If the watcher needs to do recovery work before the main sequence continues, put Pause Sequence near the start of the watcher.

## Add A Test Message

While building, make the first watcher step:

```text
Status Message Watcher fired
```

Then you can tell whether the trigger works before debugging the rest of the watcher.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The watcher never fires | Make sure the watcher is enabled and add a Status Message as the first watcher step |
| The condition is never true | Test the trigger with the same window, text, image, or value state you expect during playback |
| The watcher reacts too late | Shorten the cooldown only as much as needed |
| The main sequence keeps moving | Add Pause Sequence near the start of the watcher |
| Recovery starts after other changes already happened | Move Pause Sequence before steps that click, type, jump, or change values |
