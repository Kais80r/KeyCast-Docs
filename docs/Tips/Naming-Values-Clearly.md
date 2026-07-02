# Naming Values Clearly

Good value names make a sequence easier to understand and fix later.

## Good Names

Use names that describe what the value stores:

```text
statusText
Loops
lastResult
isReady
retryCount
windowTitle
```

## Weak Names

Avoid names that only make sense for a minute while building:

```text
value1
text2
a
thing
test
```

They work, but later it is harder to remember what they mean.

## Match The Name To The Job

Examples:

| Job | Better value name |
| --- | --- |
| Count loop runs | `Loops` |
| Store text read from the screen | `readText` |
| Remember a success/fail word | `statusText` |
| Count failed retries | `retryCount` |
| Store a yes/no state | `isReady` |

## Tip

If a value is used in Discord Message or Status Message, choose a name that makes the final message easy to read.
