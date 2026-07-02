# Examples

This folder shows complete generic patterns you can copy and adapt.

The examples avoid app-specific situations. They use neutral ideas like status text, dialogs, files, forms, dashboards, and reports.

Examples are not the only way to build something. They are starting patterns. Replace the names, text, selected areas, and step numbers with ones that match your own workflow.

## Systems

| System | Use it when | Main pieces |
| --- | --- | --- |
| [Basic Loop](Basic-Loop.md) | You want steps to repeat | Repeat X Times, Wait, Jump Sequence Step |
| [Counter Limit](Counter-Limit.md) | You want to stop after too many loop runs | Value counter, watcher or If Value |
| [Watcher Recovery](Watcher-Recovery.md) | An error can appear and recovery should retry safely | Watcher, Pause Sequence, retry counter |
| [Notification System](Notification-System.md) | You want Status or Discord messages | Status Message, Discord Message, values |

## How To Use Examples

1. Copy the structure, not the exact names.
2. Replace value names with names that match your sequence.
3. Replace text, images, areas, and step numbers.
4. Test one small part at a time before adding more logic.
5. Save the editor before closing it.

## Which Example Should I Start With?

| If your problem is... | Start with |
| --- | --- |
| Steps should repeat forever or until stopped | [Basic Loop](Basic-Loop.md) |
| A repeated workflow needs a safety limit | [Counter Limit](Counter-Limit.md) |
| A problem or disconnected state can appear while the main flow runs | [Watcher Recovery](Watcher-Recovery.md) |
| You want messages with text or live values | [Notification System](Notification-System.md) |

## Learn The Pieces

If an example uses a step you want to understand better, open that step page:

- [Steps](../Steps/README.md)
- [Values](../Values/README.md)
- [Watchers](../Watchers/README.md)
- [Guides](../Guides/README.md)
