# Open Link

Open Link opens a URL immediately using the system's normal browser or link handler.

## Fields

| Field | Meaning |
| --- | --- |
| URL | The link to open |

## Setup From Scratch

1. Add Open Link.
2. Enter the full URL.

## Example

```text
1. Open Link https://example.com
2. Wait For (Text) Dashboard timeout 30
```

## Useful For

- Opening dashboards.
- Opening documentation or tools.
- Starting browser-based workflows.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The link does not open correctly | Include `https://` or `http://` |
| The next step runs before the page is ready | Add [Wait For (Text)](Wait-For.md) or [Wait For (Window)](Wait-For.md) |
| Keyboard input goes elsewhere | Focus the browser window before pressing keys |
