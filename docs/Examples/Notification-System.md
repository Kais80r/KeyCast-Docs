# Notification System

Use this pattern when WhirlyTask should show or send an update.

Notifications are useful for progress, results, warnings, recovery, and long-running workflows. Start with Status Message while testing, then use Discord Message when you want the message outside WhirlyTask.

## What To Use

| Need | Use |
| --- | --- |
| Show a message inside WhirlyTask | Status Message |
| Send a message to Discord | Discord Message |
| Include stored text or numbers | `{ValueName}` |
| Send text read from the screen | Read Text, then Discord Message |

## Plain Discord Text

Use this when the message is always the same.

![Discord message with text](../assets/screenshots/discord-message-with-text.png)

Result in Discord:

![Discord message in Discord](../assets/screenshots/discord-message-in-discord.png)

## Discord Message With A Value

Use this when the message should include something stored in a Starting Value.

![Discord message with value](../assets/screenshots/discord-message-with-value.png)

Replace `ValueName` with the real value name from your sequence.

## Discord Message With Read Text

Use this when WhirlyTask should read visible screen text and send the result.

![Discord message with reading text value](../assets/screenshots/discord-message-with-reading-text-value.png)

The important order is:

```text
1. Read Text into ResultText
2. Discord Message {ResultText}
```

Read Text fills the value first. Discord Message sends the value after that.

Use your real value name. If the value is named `StatusText`, the message should use `{StatusText}`.

## Useful Message Ideas

- `Started`
- `Finished`
- `Error seen`
- `Current status: {statusText}`
- `Attempt {attempts}`

## Tips

- Only add messages at important points.
- Avoid sending private data unless the destination is safe.
- If a watcher sends notifications, use a cooldown to avoid repeated spam.
- If a value appears blank, check that the value was filled before the message step ran.
- Use the same capitalization in the value name and the placeholder.

## More About

- Discord step: [Discord Message](../Steps/Discord-Message.md)
- Discord setup: [Discord Webhook](../App-Features/Discord-Webhook.md)
- Values: [Values](../Values/README.md)
- Using values in text boxes: [Using Values In Text Boxes](../Tips/Using-Values-In-Text-Boxes.md)
- Reading screen text: [Read Text](../Steps/Read-Text.md)
- Local messages: [Status Message](../Steps/Status-Message.md)
- Full message guide: [Messages And Values Workflow](../Guides/Messages-And-Values-Workflow.md)
