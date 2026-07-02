# Watcher Troubleshooting

Use this page when a watcher does not behave the way you expected.

## Watcher Does Not Fire

Check:

- The sequence is running.
- The watcher state is On.
- The trigger condition is possible.
- The selected area includes the text or image.
- The cooldown is not too long.
- The value name is spelled correctly.

More detail: [Watcher Does Not Fire](../Troubleshooting/Watcher-Does-Not-Fire.md)

## Watcher Fires But The Main Sequence Keeps Running

This is normal unless the watcher reaches Pause Sequence.

Add Pause Sequence if the watcher should take over.

More detail: [Pause Sequence](Steps/Pause-Sequence.md)

## Watcher Pauses And Never Continues

After Pause Sequence, add a step that decides what happens next.

Use one of these:

- [Jump Sequence Step](../Steps/Jump-Sequence-Step.md)
- [Reset and Restart Sequence](../Steps/Reset-And-Restart-Sequence.md)
- [Stop Sequence](../Steps/Stop-Sequence.md)

More detail: [Watcher Pauses And Never Continues](../Troubleshooting/Watcher-Pauses-And-Never-Continues.md)
