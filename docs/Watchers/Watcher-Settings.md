# Watcher Settings

Watcher settings control when a watcher checks, when it can fire again, and what happens if another watcher is already running.

Use this page when a watcher fires too often, does not fire, or overlaps with another watcher in a confusing way.

## Main Settings

| Setting | Meaning |
| --- | --- |
| State | Turns the watcher on or off |
| Trigger type | What kind of condition the watcher checks |
| Trigger mode | How the condition is tested |
| Trigger value | The text, image, window, value, chance, or internet state to check |
| Area | Where screen-based triggers look |
| Scan interval | How often the watcher checks screen or window conditions |
| Cooldown | How long the watcher waits before it can fire again |
| Conflict | What to do if this watcher fires while another watcher is already running |
| After | What the watcher should do after its steps finish |

## Trigger Settings

The trigger type decides which fields matter.

| Trigger type | Common fields |
| --- | --- |
| Text | Text, mode, area, scan interval |
| Image | Image target, mode, area, scan interval |
| Window | Window title, mode, scan interval |
| Sequence Value | Value name, compare mode, compare text |
| Chance | Percent chance |
| Internet | Online or offline mode, scan interval |

For details on each trigger, see [Triggers](Triggers/README.md).

## State

State controls whether the watcher is active.

| State | Result |
| --- | --- |
| On | The watcher can fire while the sequence runs |
| Off | The watcher is saved but ignored during playback |

Turn a watcher off when you want to keep it for later but do not want it affecting the current test.

## Scan Interval

Scan interval controls how often WhirlyTask checks a trigger that needs polling.

Short intervals react faster, but they can cost more work and may fire during temporary screen changes.

Long intervals are calmer, but the watcher can feel slower.

## Cooldown

Cooldown controls how long the watcher waits after firing before it can fire again.

Use a longer cooldown when:

- the same warning stays on screen
- Discord or status messages repeat too often
- recovery steps need time to finish
- a connection or window state flickers

## Conflict

Conflict controls what happens when this watcher fires while another watcher is already running.

| Conflict option | Meaning |
| --- | --- |
| Ignore | Do not start this watcher while another watcher is running |
| Stop watcher | Let this watcher take over and stop the current watcher path |
| Run alongside | Let this watcher run while the other watcher continues |

## Choosing A Conflict Option

Use `Ignore` for most recovery watchers. It prevents two recovery paths from fighting over the same app.

Use `Stop watcher` when the new watcher is more important than the current one. For example, an emergency stop watcher should interrupt a slower notification watcher.

Use `Run alongside` for small side effects that are safe to overlap, such as status messages or independent Discord alerts.

## After

After controls what happens once watcher steps finish.

If the watcher never uses [Pause Sequence](Steps/Pause-Sequence.md), the main sequence usually keeps going while the watcher runs.

If the watcher uses Pause Sequence, make sure the watcher steps clearly continue, reset, or stop the sequence.

## Good Defaults

| Watcher purpose | State | Cooldown | Conflict |
| --- | --- | --- | --- |
| Popup recovery | On | 5 to 15 seconds | Ignore |
| Discord notification | On | 30 seconds or more | Run alongside |
| Emergency stop | On | 1 to 5 seconds | Stop watcher |
| Testing a new watcher | On | 3 to 10 seconds | Ignore |

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Watcher does not fire | Check State, trigger fields, area, scan interval, and cooldown |
| Watcher fires repeatedly | Increase Cooldown |
| Two watchers fight each other | Use `Ignore` or `Stop watcher` instead of `Run alongside` |
| Recovery starts too slowly | Lower Scan interval carefully |
| Main steps keep running during recovery | Add [Pause Sequence](Steps/Pause-Sequence.md) near the start of watcher steps |

## More About

- Watcher overview: [Watchers](README.md)
- Trigger types: [Triggers](Triggers/README.md)
- Taking over the main sequence: [Pause Sequence](Steps/Pause-Sequence.md)
- Watcher troubleshooting: [Watcher Troubleshooting](Troubleshooting.md)
