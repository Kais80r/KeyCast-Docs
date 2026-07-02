# Values

Values let a sequence remember information.

A value is a named text field. Steps can put text into it, change it, compare it, or use it in messages.

Values are one of the most important parts of sequences because they connect steps together. One step can read or create information, and another step can use it later.

Think of a value like a named box:

```text
statusText = Ready
attempts = 3
```

The name lets other steps find the box again.

## Start Here

| Page | What it explains |
| --- | --- |
| [What Is A Value](What-Is-A-Value.md) | The basic idea |
| [Using Values In Messages](Using-Values-In-Messages.md) | How `{ValueName}` works |
| [Reading Text Into Values](Reading-Text-Into-Values.md) | How Read Text stores screen text |
| [Using Values In Text Boxes](../Tips/Using-Values-In-Text-Boxes.md) | Where `{ValueName}` can be typed into step fields |

## Value Life Cycle

| Moment | What happens |
| --- | --- |
| Sequence starts | Each value gets its Starting Value |
| A step reads, sets, or changes a value | The value stores the new text |
| A later step uses `{ValueName}` | WhirlyTask replaces the placeholder with the current value |
| Reset and Restart Sequence runs | Values return to their Starting Values |

## Example

```text
Starting value:
statusText starts as empty

Main step:
Read Text into statusText

Message:
Current status: {statusText}
```

The value starts empty. Read Text fills it. The message uses it.

## What Values Can Be Used For

- Store text read from the screen.
- Count attempts in a loop.
- Remember whether something is ready, waiting, failed, or complete.
- Send live information in Status Message or Discord Message.
- Let If Sequence Value choose a branch.
- Let watchers react to changing state.

## Common Value Systems

| System | Pages |
| --- | --- |
| Read text into a value | [Reading Text Into Values](Reading-Text-Into-Values.md) |
| Loop counter | [Counter Limit](../Examples/Counter-Limit.md) |
| Retry counter | [Change Sequence Value](../Steps/Change-Sequence-Value.md) |
| Message with live text | [Notification System](../Examples/Notification-System.md) |

## Which Value Step Should I Use?

| Need | Use |
| --- | --- |
| Put exact text into a value | [Set Sequence Value](../Steps/Set-Sequence-Value.md) |
| Add or subtract from a counter | [Change Sequence Value](../Steps/Change-Sequence-Value.md) |
| Read visible screen text into a value | [Read Text](../Steps/Read-Text.md) |
| Check a value and choose a branch | [If Sequence Value](../Steps/If-Sequence-Value.md) |
| React when a value changes in the background | [When Sequence Value](../Watchers/Triggers/When-Sequence-Value.md) |

## Good Value Names

Use clear names with no spaces.

Good:

```text
statusText
resultText
attempts
isReady
lastMessage
```

Avoid:

```text
value1
thing
x
text
```

Temporary names are fine while testing, but clear names make old sequences easier to fix.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| A placeholder is not replaced | Match the value name exactly, including capitalization |
| A message or check is blank | Fill the value before using it |
| Number comparisons fail | Make sure the value contains only the number you want to compare |
| Values reset unexpectedly | Check whether Reset and Restart Sequence returned them to their Starting Values |
| The sequence is hard to fix later | Use clear value names that describe what each value stores |

## More About

- [Getting Started](../Getting-Started.md)
- [Glossary](../Glossary.md)
- [Using Values In Messages](Using-Values-In-Messages.md)
- [Value Is Blank](../Troubleshooting/Value-Is-Blank.md)
