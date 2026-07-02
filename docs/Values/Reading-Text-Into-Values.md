# Reading Text Into Values

Read Text stores screen text in a value.

Later steps can use the saved text in messages, checks, and other text fields.

## Basic Setup

```text
Starting value:
resultText starts as empty

Main step:
Read Text from selected area into resultText

Message:
Read result: {resultText}
```

## Use The Value Later

After Read Text fills the value, you can use it in:

- Status Message
- Discord Message
- If Value
- Watcher triggers
- Other steps that accept value placeholders

## Testing

Always test Read Text with a message first.

```text
1. Read Text into resultText
2. Status Message {resultText}
3. Stop
```

When the message shows the correct text, use the value in the real workflow.

## More About

- Read Text step: [Read Text](../Steps/Read-Text.md)
- Values overview: [Values](README.md)
- Using values in text boxes: [Using Values In Text Boxes](../Tips/Using-Values-In-Text-Boxes.md)
- Checking read text with a branch: [If Sequence Value](../Steps/If-Sequence-Value.md)
- Read Text troubleshooting: [Read Text Is Wrong](../Troubleshooting/Read-Text-Is-Wrong.md)
