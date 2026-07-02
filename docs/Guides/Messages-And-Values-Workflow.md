# Messages And Values Workflow

This guide explains how to send useful messages from a sequence.

Messages can be shown inside WhirlyTask with Status Message or sent to Discord with Discord Message. Both can include values like `{ValueName}`.

## Message Types

| Message type | Use when |
| --- | --- |
| Status Message | You want local progress while building or running |
| Discord Message | You want a message in a Discord server channel |

Start with Status Message while testing. Switch to Discord Message after the text is correct.

## Plain Text Message

![Discord message with text](../assets/screenshots/discord-message-with-text.png)

```text
1. Status Message Starting workflow
```

or:

```text
1. Discord Message Workflow started
```

Plain text is useful for start, finish, error, and recovery messages.

## Message With A Value

![Discord message with value](../assets/screenshots/discord-message-with-value.png)

```text
Starting Values:
resultText starts as empty

Main Steps:
1. Read Text resultText from selected area
2. Status Message Result: {resultText}
```

When the step runs, `{resultText}` is replaced with the current value.

If the value was filled by Read Text first, the same placeholder works:

![Discord message with reading text value](../assets/screenshots/discord-message-with-reading-text-value.png)

## Discord Setup

Discord messages need a webhook first.

The normal Discord path is:

```text
Discord server > text channel settings > Integrations > Webhooks
```

The webhook must come from a server text channel, not a direct message.

After copying the webhook URL, open:

```text
WhirlyTask Menu > Discord Webhook > Set Webhook...
```

Then use Test Message before adding Discord Message steps to a sequence.

More detail: [Discord Webhook](../App-Features/Discord-Webhook.md)

Example result in Discord:

![Discord message in Discord](../assets/screenshots/discord-message-in-discord.png)

## Useful Message Examples

| Situation | Message text |
| --- | --- |
| Sequence started | `Workflow started` |
| Value was read | `Read: {resultText}` |
| Attempt counter | `Attempt {attempts}` |
| Watcher fired | `Recovery started: {statusText}` |
| Sequence finished | `Workflow finished` |

## Avoid Message Spam

Messages inside loops or watchers can repeat quickly.

To reduce spam:

1. Use a longer watcher cooldown.
2. Send messages only when state changes.
3. Use Status Message during testing before Discord Message.
4. Put Discord Message after a successful read or final decision, not before every small step.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Discord message does not send | Set up the webhook, then run Test Message |
| Value is blank | Make sure the value exists and is filled before the message step runs |
| `{ValueName}` appears literally | Check the placeholder spelling and braces |
| Too many messages appear | Increase cooldowns or move the message outside repeated steps |
| Message contains private information | Remove the value or change the message before sending it |

## More About

- [Status Message](../Steps/Status-Message.md)
- [Discord Message](../Steps/Discord-Message.md)
- [Discord Webhook](../App-Features/Discord-Webhook.md)
- [Using Values In Text Boxes](../Tips/Using-Values-In-Text-Boxes.md)
- [Notification System](../Examples/Notification-System.md)
