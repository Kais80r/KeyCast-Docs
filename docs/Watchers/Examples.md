# Watcher Examples

These examples are generic patterns. Replace the text, values, areas, and step numbers with your own workflow.

## Show A Message When Text Appears

Use this when the main sequence can keep running.

```text
Watcher trigger:
When Text Complete is seen

Watcher steps:
1. Status Message Complete appeared
```

## Pause And Handle A Popup

Use this when the popup should interrupt the normal workflow.

```text
Watcher trigger:
When Text Confirm is seen

Watcher steps:
1. Pause Sequence
2. Click Text Confirm
3. Jump Sequence Step 4
```

## React To A Value

Use this when a value is filled by another step.

```text
Starting value:
statusText starts as empty

Main step:
Read Text into statusText

Watcher trigger:
When Sequence Value statusText contains Ready

Watcher steps:
1. Status Message Ready state found
```

## Retry After A Problem

Use this when the workflow should start again after a known problem.

```text
Watcher trigger:
When Text Try again is seen

Watcher steps:
1. Pause Sequence
2. Click Text Try again
3. Reset and Restart Sequence
```

## More Complete Examples

- [Watcher Recovery](../Examples/Watcher-Recovery.md)
- [Watcher Recovery Workflow](../Guides/Watcher-Recovery-Workflow.md)
- [Counter Limit](../Examples/Counter-Limit.md)
