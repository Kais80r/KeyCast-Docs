# Watcher Triggers

A trigger is the condition that makes a watcher fire.

The watcher checks the trigger repeatedly while the sequence is running. When the trigger becomes true, the watcher runs its steps.

Choose the trigger by asking what kind of thing should cause the reaction.

## Trigger Pages

| Trigger | Use when |
| --- | --- |
| [What Is A Trigger](What-Is-A-Trigger.md) | You want the basic idea |
| [When Text](When-Text.md) | Visible text appears on the screen |
| [When Image](When-Image.md) | A stable image or icon appears |
| [When Sequence Value](When-Sequence-Value.md) | A stored value matches or changes |
| [When Window](When-Window.md) | A window or app state matters |
| [When Internet](When-Internet.md) | Connection state matters |
| [For Chance](For-Chance.md) | You want a random or occasional trigger |

## Which Trigger Should I Choose?

| You want to react to... | Use |
| --- | --- |
| A word or phrase appearing on screen | [When Text](When-Text.md) |
| A stable icon, button, or visual element | [When Image](When-Image.md) |
| A value containing text, reaching a number, or changing | [When Sequence Value](When-Sequence-Value.md) |
| A window opening, closing, or existing | [When Window](When-Window.md) |
| Internet going online or offline | [When Internet](When-Internet.md) |
| A random chance | [For Chance](For-Chance.md) |

## Trigger Timing

Some triggers scan the screen every few seconds. Some check stored values. The cooldown decides how soon the same watcher can fire again after it already ran.

If a watcher fires too often, increase the cooldown.

If a watcher feels slow, lower the scan interval or cooldown carefully.

## Trigger Reliability

| Trigger type | Reliability tip |
| --- | --- |
| Text | Use a unique phrase and avoid tiny selected areas |
| Image | Capture only the stable part of the image |
| Sequence Value | Print the value with `{ValueName}` while testing |
| Window | Use a window title or app state that stays consistent |
| Internet | Add a cooldown so short connection changes do not spam recovery |
| Chance | Keep chance-based behavior away from important safety logic |

## More About

- [Watchers](../README.md)
- [Keeping Watchers Predictable](../../Tips/Keeping-Watchers-Predictable.md)
- [Watcher Does Not Fire](../../Troubleshooting/Watcher-Does-Not-Fire.md)
