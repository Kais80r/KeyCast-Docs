# Glossary

This page explains the words used in WhirlyTask and in these docs.

## Main Item Types

| Word | Meaning |
| --- | --- |
| Track | A recorded keyboard and mouse action that can be replayed |
| Advanced Track | An editable reusable step list |
| Sequence | A full workflow with main steps, starting values, and optional watchers |

## Sequence Words

| Word | Meaning |
| --- | --- |
| Step | One action inside a sequence or advanced track |
| Main Steps | The normal path of a sequence |
| Starting Values | Values that exist when the sequence starts |
| Value | A named piece of text stored by the sequence |
| Watcher | A background check inside a sequence |
| Trigger | The condition that makes a watcher run |
| Cooldown | How long a watcher waits before it can fire again |
| Branch | A path inside an If step, usually Then or Else |
| Loop | Steps that jump back and repeat |

## Screen Words

| Word | Meaning |
| --- | --- |
| Selected area | A rectangle on the screen that WhirlyTask should scan or use |
| Full Screen | The whole screen is scanned |
| Screen text reading | Reading visible letters from an image of the screen |
| OCR | The technical name for screen text reading |
| Image matching | Looking for a saved visual target on the screen |

## Message Words

| Word | Meaning |
| --- | --- |
| Status Message | A message shown inside WhirlyTask |
| Discord Message | A message sent to a Discord channel through a webhook |
| Webhook | A special Discord URL that lets WhirlyTask post into one server channel |
| Placeholder | Text like `{ValueName}` that gets replaced with a sequence value |

## Control Words

| Word | Meaning |
| --- | --- |
| Pause Sequence | A watcher step that lets the watcher take control from the main sequence |
| Jump Sequence Step | Move the main sequence to a specific step number |
| Jump Block Step | Move inside the current block, such as inside Then or Else |
| Reset and Restart Sequence | Reset all values to their starting values and begin the sequence again |
| Stop Sequence | End playback |
| Return to Sequence | Leave an advanced track and continue the sequence that called it |

## Protection Words

| Word | Meaning |
| --- | --- |
| Crash Protection | Stops playback if a selected app or window closes |
| Text Protection | Stops playback if specific text appears on the screen |
| Emergency Stop | The hotkey used to stop playback immediately |

## More About

- [Getting Started](Getting-Started.md)
- [Basics](Basics/README.md)
- [Steps](Steps/README.md)
- [Watchers](Watchers/README.md)
- [Values](Values/README.md)
