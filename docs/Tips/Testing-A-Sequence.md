# Testing A Sequence

Test a sequence in small parts instead of building the whole thing first.

## A Good Testing Flow

1. Add the first few steps.
2. Add a Status Message that says what should be happening.
3. Run the sequence.
4. Fix problems before adding more steps.
5. Save the editor when the part works.

## Why This Helps

If ten new steps are added at once, it is hard to know which one caused the problem.

If one or two steps are added at a time, the broken part is usually obvious.

## Useful Test Messages

```text
Reached step 4
Current value: {statusText}
Loop count: {Loops}
Watcher fired
Text found: {readText}
```

## Good Signs

- The status message changes when you expect it to.
- Values show the text or number you expected.
- Wait steps finish only after the real condition appears.
- Watchers fire once, then respect their cooldown.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Changes disappear | Press Save before closing the editor or testing from the main window |
| Discord messages are wrong | Test the same text with Status Message first |
| You cannot tell whether a watcher fired | Add a Status Message as the first watcher step |
| Testing is too fast to understand | Use longer waits and cooldowns until the sequence is stable |
