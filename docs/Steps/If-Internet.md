# If Internet

If Internet checks whether the connection state is online or offline, then runs the Then branch or Else branch.

## Fields

| Field | Meaning |
| --- | --- |
| Mode | `is online` or `is offline` |
| Then branch | Steps to run when the condition is true |
| Else branch | Steps to run when the condition is false |

## Setup From Scratch

1. Add If Internet.
2. Choose `is online` or `is offline`.
3. Add a small Status Message in both branches while testing.
4. Add the real online/offline actions.

## Example

```text
If Internet is online
Then:
1. Open Link https://example.com
Else:
1. Status Message Waiting for connection
2. Wait For (Internet) is online timeout 60
```

## Useful For

- Choosing between online and offline behavior.
- Avoiding network actions while offline.
- Showing a message when the connection is unavailable.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| A specific website still does not load | Add a later check for the page or app text you expect |
| The sequence checks too early | Use [Wait For (Internet)](Wait-For.md) when you need to wait for connectivity |
| Offline mode has no recovery | Add steps in the offline branch to wait, retry, notify, or stop |
