# Samples

The samples folder contains more subfolders:

- [Gameplay](#gameplay)
- [UI](#user-interface)

## Gameplay

Located in the `Samples/Gameplay` folder, these change the sounds for when a key is pressed, you miss a note, etc.

| Sample             | Usage                                                         |
| ------------------ | ------------------------------------------------------------- |
| `fail.wav`         | Failing for any reason.                                       |
| `hit.wav`          | Pressing a key.                                               |
| `miss.wav`         | Missing a note.                                               |
| `restart.wav`      | Restarting the game either via the pause menu or quick retry. |
| `full-combo.wav`   | Finishing a map with no misses.                               |
| `all-flawless.wav` | Finishing a map with only Flawless judgements.                |

You can have multiple miss sounds, and the game will randomly pick one among all the samples you have put. Make sure the first four letters are "miss" in the file name, and whatever comes after will be ignored.

- Names like `miss test.wav`, `misster.wav`, `miss-alt.wav`, and `missssssss.wav` will work.
- Names like `another miss.wav`, `mis.wav`, and `mis1.wav` will **not** work.

## User Interface

Located in `Samples/UI`, these change the sounds when hovering, clicking etc.

| Sample                  | Usage                                                    |
| ----------------------- | -------------------------------------------------------- |
| `back.wav`              | Exiting a screen.                                        |
| `select.wav`            | Pressing play in song select or when entering main menu. |
| `hover.wav`             | Hovering over buttons or similar.                        |
| `click.wav`             | Clicking on buttons or similar.                          |
| `click-disabled.wav`    | Clicking on a button that is disabled.                   |
| `skin-select-click.wav` | Played when selecting the skin in settings.              |
