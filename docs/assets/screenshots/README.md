# Screenshot Checklist

Put documentation screenshots in this folder.

Recommended image names:

| File | What to capture |
| --- | --- |
| `main-window.png` | Main WhirlyTask window with a generic loaded item |
| `library.png` | Library window showing saved item types |
| `track-editor.png` | Track editor with a short generic recorded action |
| `advanced-track-editor.png` | Advanced Track editor with a reusable action block |
| `sequence-editor.png` | Sequence editor with starting values, main steps, and a watcher |
| `step-menu.png` | Add Step menu showing available step categories |
| `app-features-menu.png` | Main menu showing protection, Discord, recording, hotkey, loop, and help options |
| `crash-protection-menu.png` | Crash Protection submenu with a generic selected window |
| `text-protection-menu.png` | Text Protection submenu with generic protected text |
| `discord-webhook-menu.png` | Discord Webhook submenu without exposing the webhook URL |
| `simple-discord-message.png` | Plain Discord Message steps with start and end messages |
| `status-message-step.png` | Status Message step row with plain text |
| `status-message-output.png` | Main WhirlyTask window showing the status message result |
| `discord-message-with-text.png` | Single Discord Message step with plain text |
| `discord-message-in-discord.png` | Result of a Discord Message inside Discord |
| `discord-message-with-value.png` | Discord Message using a typed value placeholder like `{ValueName}` |
| `discord-message-with-reading-text-value.png` | Read Text into a value, then Discord Message sends that value |
| `read-text-step.png` | Read Text step showing area and destination value |
| `area-picker.png` | Area selection overlay around generic text |
| `reconnect-tries-value.png` | Starting Value row for a reconnect retry counter |
| `reconnect-watcher-without-retry-limit.png` | Reconnect watcher before adding a retry limit |
| `reconnect-watcher-with-retry-limit.png` | Reconnect watcher with a retry counter and stop limit |
| `watcher-note.png` | Watcher note strip under the watcher header |
| `watcher-pause-sequence.png` | Watcher with Pause Sequence and a continuation step |

Tips:

- Use PNG files.
- Use generic examples and avoid private or app-specific data.
- Hide webhook URLs, tokens, usernames, local paths, and personal data.
- Crop enough of the window so the UI has context.
- Keep screenshots readable at documentation page width.

Example image path:

```text
docs/assets/screenshots/sequence-editor.png
```
