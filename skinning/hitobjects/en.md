# HitObjects
These are the files that determine how the notes themselves look. For these HitObjects, they're broken down into 4 more folders: `LongNoteBody`, `LongNoteEnd`, `Note` and `Tick`.

The files within these folders should be named as such: `{element}/{key}k-{lane}.png`

- `{element}` refers to which part of the note you're skinning.
- `{key}` refers to what gamemode this element belongs to.
- `{lane}` refers to what lane in that gamemode it appears in, numbered from left to right.

|Element|Used for...|
|---|---|
|LongNoteBody|Middle of Long Notes|
|LongNoteEnd|End of Long Notes|
|Note|Both the Note itself and the start of Long Notes|
|Tick|Tick Notes|

As an example, `Note/7k-4.png` will skin the Note in the 4th (middle) lane of a 7-key stage. For easier readability between transitions, it is advised to have the multiple keymode skin elements match each other. Keep in mind that `LongNoteBody` will get stretched according to the length of the Long Note it's in.