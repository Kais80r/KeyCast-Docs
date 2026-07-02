# Watcher Steps

Watcher steps are the actions that run after a watcher trigger becomes true.

Most step ideas work the same way inside a watcher as they do in the main sequence. The special one to understand is Pause Sequence.

## Pages

| Page | What it explains |
| --- | --- |
| [Pause Sequence](Pause-Sequence.md) | How a watcher takes over from the main sequence |

## Quick Rule

If the watcher only sends a message or performs a small side action, it may not need Pause Sequence.

If the watcher should stop the normal path and handle a problem first, it should usually use Pause Sequence.
