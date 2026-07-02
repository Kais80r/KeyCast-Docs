# Troubleshooting

Start here when something does not work.

Pick the page that matches the problem you see.

## First 60-Second Checks

Before changing many things, check these:

1. Press Save in the editor if you want the changes to apply.
2. Make sure the correct window is focused.
3. Test the failing step by itself.
4. Add a Status Message before and after the failing step.
5. Print important values with `{ValueName}`.
6. If text or image detection fails, test Full Screen once, then adjust the selected area.

## Symptoms

| What you notice | Start here |
| --- | --- |
| Text is read wrong, partly missing, or split strangely | [Read Text Is Wrong](Read-Text-Is-Wrong.md) |
| Text reading works only with a bigger area | [Selected Area Problems](Selected-Area-Problems.md) |
| The automation clicks the wrong text | [Text Clicks Wrong Place](Text-Clicks-Wrong-Place.md) |
| A watcher never fires | [Watcher Does Not Fire](Watcher-Does-Not-Fire.md) |
| A watcher pauses and then gets stuck | [Watcher Pauses And Never Continues](Watcher-Pauses-And-Never-Continues.md) |
| A value in a message is empty | [Value Is Blank](Value-Is-Blank.md) |
| Editor changes vanish after closing | [Editor Changes Disappear](Editor-Changes-Disappear.md) |
| Keys or clicks go to another app | [Wrong Window Or Focus](Wrong-Window-Or-Focus.md) |
| Playback stops because a protected app closed | [Crash Protection](../App-Features/Crash-Protection.md) |
| Playback stops because protected text appeared | [Text Protection](../App-Features/Text-Protection.md) |

## Text And Screen Reading

| Problem | Open this |
| --- | --- |
| Read Text gives wrong text | [Read Text Is Wrong](Read-Text-Is-Wrong.md) |
| Read Text gives nothing | [Read Text Finds Nothing](Read-Text-Finds-Nothing.md) |
| A selected area works only when it is bigger | [Selected Area Problems](Selected-Area-Problems.md) |
| Click Text clicks the wrong place | [Text Clicks Wrong Place](Text-Clicks-Wrong-Place.md) |

## Images

| Problem | Open this |
| --- | --- |
| Click Image or If Image does not find the target | [Image Not Found](Image-Not-Found.md) |

## Watchers

| Problem | Open this |
| --- | --- |
| Watcher does not fire | [Watcher Does Not Fire](Watcher-Does-Not-Fire.md) |
| Watcher pauses but never continues | [Watcher Pauses And Never Continues](Watcher-Pauses-And-Never-Continues.md) |
| Watcher does not pause the main sequence | [Watcher Does Not Pause](Watcher-Does-Not-Pause.md) |

## Values And Editor

| Problem | Open this |
| --- | --- |
| A value or placeholder is blank | [Value Is Blank](Value-Is-Blank.md) |
| Editor changes disappear | [Editor Changes Disappear](Editor-Changes-Disappear.md) |
| Key presses go to the wrong app | [Wrong Window Or Focus](Wrong-Window-Or-Focus.md) |

## App Features

| Problem | Open this |
| --- | --- |
| Playback stops when a selected app/window closes | [Crash Protection](../App-Features/Crash-Protection.md) |
| Playback stops when specific text appears | [Text Protection](../App-Features/Text-Protection.md) |
| Discord messages or alerts do not send | [Discord Webhook](../App-Features/Discord-Webhook.md) |
| Recorded tracks include too much or too little input | [Recording Options](../App-Features/Recording-Options.md) |
| Loop only works sometimes | [Playback, Speed, And Loop](../App-Features/Playback-Speed-And-Loop.md) |

## General Debug Pattern

1. Test one step at a time.
2. Add Status Message before and after the step.
3. Print values with `{ValueName}`.
4. Use Full Screen once, then try a selected area.
5. Save before closing the editor.

## When To Use A Different Tool

| If this keeps happening | Consider |
| --- | --- |
| A recorded track fails because the app is not ready | Use a sequence with Wait For (Text) or Wait For (Window) |
| Text Protection stops on harmless text | Use a more specific phrase or a watcher with custom logic |
| Read Text is too unstable for one tiny area | Make the area larger or use If Text for a known phrase |
| A watcher is doing normal workflow logic | Move that logic into main steps |
| Discord messages are too noisy | Increase watcher cooldown or send fewer messages |

## Helpful References

- [Getting Started](../Getting-Started.md)
- [Build A Reliable Sequence](../Guides/Build-A-Reliable-Sequence.md)
- [Steps](../Steps/README.md)
- [Values](../Values/README.md)
- [Watchers](../Watchers/README.md)
