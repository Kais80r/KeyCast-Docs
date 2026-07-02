# Watcher Does Not Fire

This page is for watchers that never run their steps.

## Check The Basics

- The sequence is running.
- The watcher state is On.
- The trigger condition is possible.
- The cooldown is not hiding repeated tests.
- The selected area includes the target.
- The value name is spelled correctly.

## Test The Watcher

Add a simple first step:

```text
Status Message Watcher fired
```

If you never see that message, the trigger is not firing.

If you do see it, the trigger works and the problem is later in the watcher steps.

## Value Watcher Checks

If the trigger uses a sequence value:

- Print the value with `{ValueName}`.
- Use `contains` if the value has extra text.
- Use `changed` only when a step changes the value during the run.
- Remember that a starting value is not the same as a changed value.

## More About

- Watchers: [Watchers](../Watchers/README.md)
- Watcher triggers: [Triggers](../Watchers/Triggers/README.md)
- Value watcher trigger: [When Sequence Value](../Watchers/Triggers/When-Sequence-Value.md)
- Text watcher trigger: [When Text](../Watchers/Triggers/When-Text.md)
- Watcher tips: [Keeping Watchers Predictable](../Tips/Keeping-Watchers-Predictable.md)
