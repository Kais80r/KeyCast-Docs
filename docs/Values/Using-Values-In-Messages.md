# Using Values In Messages

Use braces to insert a value into a message.

Example:

```text
Current status: {statusText}
```

If `statusText` contains `Ready`, the message becomes:

```text
Current status: Ready
```

This works in both [Status Message](../Steps/Status-Message.md) and [Discord Message](../Steps/Discord-Message.md).

## Setup From Scratch

1. Create the value in Starting Values.
2. Fill or change the value before the message step runs.
3. Add Status Message or Discord Message.
4. Type the value name inside braces.

Example:

```text
Starting Values:
resultText starts as empty

Main Steps:
1. Read Text resultText
2. Discord Message Result: {resultText}
```

## Good Debug Messages

When building a sequence, add messages that show the current value.

Examples:

```text
Text read: {resultText}
Attempts: {attempts}
State: {isReady}
```

## If A Placeholder Is Blank

Check:

- The value exists in Starting Values.
- The name is spelled the same way.
- A step filled the value before the message ran.
- Reset and Restart Sequence did not reset the value before the message ran.

More detail: [Value Is Blank](../Troubleshooting/Value-Is-Blank.md)

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The placeholder appears literally | Remove spaces inside the braces, like `{resultText}` |
| The wrong capitalization is used | Match the value name exactly, such as `{resultText}` |
| The message is blank | Run Read Text or Set Sequence Value before the message |
| The value was reset | Check whether Reset and Restart Sequence ran before the message |

## More About

- Values overview: [Values](README.md)
- Using values in text boxes: [Using Values In Text Boxes](../Tips/Using-Values-In-Text-Boxes.md)
- Discord messages: [Discord Message](../Steps/Discord-Message.md)
- Status messages: [Status Message](../Steps/Status-Message.md)
