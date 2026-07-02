# Discord Webhook

Discord Webhook lets WhirlyTask send messages to a Discord text channel.

This is used by:

- [Discord Message](../Steps/Discord-Message.md) steps.
- Crash Protection alerts.
- Text Protection alerts.
- Test messages from the menu.

## Important Requirement

The message must go to a Discord server channel.

A webhook is created inside a server channel. It is not created from a normal direct message.

You also need permission in that server/channel to manage webhooks. Missing webhook options usually mean the permission is unavailable.

## Get A Webhook URL In Discord

Discord's labels can move a little over time, but the normal path is:

```text
Discord server > text channel settings > Integrations > Webhooks
```

Step by step:

1. Open Discord.
2. Click the server where you want WhirlyTask messages to appear.
3. Choose the text channel that should receive the messages.
4. Open that channel's settings. This is usually the small gear icon next to the channel name.
5. Open `Integrations`.
6. Open `Webhooks`.
7. Choose `New Webhook` or `Create Webhook`.
8. Give the webhook a clear name, such as `WhirlyTask`.
9. Make sure it is assigned to the correct channel.
10. Click `Copy Webhook URL`.

That copied URL is what you paste into WhirlyTask.

## Set The Webhook In WhirlyTask

Open:

```text
Menu > Discord Webhook
```

Then:

1. Click `Set Webhook...`.
2. Paste the Discord webhook URL.
3. Click OK.
4. Click `Test Message`.

If the test sends successfully, WhirlyTask queues a test message and shows:

```text
Discord test queued.
```

You should then see a test message appear in the Discord channel.

## Menu Options

The WhirlyTask menu shows:

- `Set Webhook...`
- `Test Message`
- `Clear Webhook`
- current status

## Using Discord Message Steps

After the webhook is set, use the [Discord Message](../Steps/Discord-Message.md) step in a sequence.

Plain text:

```text
Discord Message Workflow finished
```

Text with values:

```text
Discord Message Current status: {statusText}
```

## Protection Alerts

Crash Protection and Text Protection each have their own `Discord Message` toggle.

Those toggles only decide whether a protection stop sends Discord alerts. Normal Discord Message steps use the webhook separately.

## Troubleshooting

| Problem | What to check |
| --- | --- |
| No message appears in Discord | Make sure you are looking in the server text channel, not a direct message |
| You cannot create a webhook | Check that you have permission to manage webhooks in that channel |
| Test Message does not send | Set the webhook again, paste the full URL, then run Test Message |
| Messages worked before but stopped | Check whether the Discord channel or webhook was deleted |
| A message includes private data | Remove the value or change the message before sending it to Discord |
| Watcher messages repeat too often | Increase the watcher cooldown or move the message outside the repeated path |

## Safety Tips

- Keep the webhook URL private.
- Treat the webhook URL like a password for posting into that channel.
- If the URL leaks, delete the webhook in Discord and create a new one.
- Keep secrets, tokens, personal data, and private paths out of messages.

## Testing Tips

- Use `Test Message` after setting the webhook.
- Test message text with [Status Message](../Steps/Status-Message.md) before sending real Discord messages.
- Use watcher cooldowns for alerts that can trigger repeatedly.
