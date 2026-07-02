# Tips

Tips are short practical pages for building cleaner automations and avoiding common mistakes.

Use these when something technically works, but you want it to be more reliable, easier to test, or easier to understand later.

Tips are different from troubleshooting pages. Troubleshooting starts when something is broken. Tips help you build in a cleaner way before it breaks.

## Quick Tips

| Tip | Use it when |
| --- | --- |
| [Testing A Sequence](Testing-A-Sequence.md) | You are building or debugging a sequence |
| [Making Areas Reliable](Making-Areas-Reliable.md) | Text or image detection misses small selected areas |
| [Using Status Messages While Building](Using-Status-Messages-While-Building.md) | You need to see what the automation is doing |
| [Using Values In Text Boxes](Using-Values-In-Text-Boxes.md) | You want text boxes to use stored values like `{statusText}` |
| [Naming Values Clearly](Naming-Values-Clearly.md) | A sequence uses multiple values |
| [Keeping Watchers Predictable](Keeping-Watchers-Predictable.md) | Watchers fire too often, too late, or at confusing times |

## Tips By Area

| Area | Helpful tips |
| --- | --- |
| Building | [Testing A Sequence](Testing-A-Sequence.md), [Using Status Messages While Building](Using-Status-Messages-While-Building.md) |
| Screen reading | [Making Areas Reliable](Making-Areas-Reliable.md) |
| Values | [Using Values In Text Boxes](Using-Values-In-Text-Boxes.md), [Naming Values Clearly](Naming-Values-Clearly.md) |
| Watchers | [Keeping Watchers Predictable](Keeping-Watchers-Predictable.md) |

## Best First Habits

- Build one small part at a time.
- Test with Status Message before using Discord Message.
- Use values with names that explain what they store.
- Use `{ValueName}` when a text box should use a stored value.
- Give screen areas a little padding around text or images.
- Use watchers for unexpected events, not for the normal path.
- Save the editor before closing if you want changes to apply.

## More About

- [Getting Started](../Getting-Started.md)
- [Build A Reliable Sequence](../Guides/Build-A-Reliable-Sequence.md)
- [Troubleshooting](../Troubleshooting/README.md)
