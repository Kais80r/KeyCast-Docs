# Return to Sequence

Return to Sequence exits an advanced track and returns control to the sequence that called it.

## Where It Appears

This step is available when editing an advanced track.

## Fields

This step has no fields.

## Setup From Scratch

1. Open an advanced track.
2. Add Return to Sequence where the advanced track should hand control back.
3. In the calling sequence, put the next step after Run Advanced Track.

## Example

```text
Advanced track:
1. Press Key Ctrl+S
2. Return to Sequence

Sequence:
1. Run Advanced Track Save Work
2. Status Message Save track finished
```

## Troubleshooting

| Problem | What to try |
| --- | --- |
| The main sequence should continue | Use Return to Sequence instead of Stop Sequence inside an advanced track |
| You need to jump to a specific main step | Use [Jump Sequence Step](Jump-Sequence-Step.md) from the sequence flow |
| The step is in a normal sequence | Remove it unless the step is inside an advanced track called by a sequence |
