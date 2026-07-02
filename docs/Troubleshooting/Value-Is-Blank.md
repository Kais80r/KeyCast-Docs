# Value Is Blank

This page is for messages like `{statusText}` showing nothing, or conditions not seeing a value.

## Check These First

- The value exists in Starting Values.
- The name is spelled the same everywhere.
- Read Text or Set Value ran before the value was used.
- Reset and Restart Sequence did not reset the value before this step ran.
- The Read Text area actually found text.

## Good Test

```text
1. Set Value statusText to Testing
2. Status Message {statusText}
3. Stop
```

If this works, the value system is working. The issue is probably the step that should fill the value.

## More About

- Values: [Values](../Values/README.md)
- Using values in text boxes: [Using Values In Text Boxes](../Tips/Using-Values-In-Text-Boxes.md)
- Reading text into values: [Reading Text Into Values](../Values/Reading-Text-Into-Values.md)
- Read Text step: [Read Text](../Steps/Read-Text.md)
