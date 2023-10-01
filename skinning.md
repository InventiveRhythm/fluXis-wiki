# Skinning

To begin skinning, go to Settings -> Appearance -> Open Skin folder, or navigate to `C:\Users\USER\AppData\Roaming\fluXis\` and create a "Skins" folder.

There's 5 different sections that go into each skin, alongside the [skin.json](#json) itself. These are the [HitObjects](#hitobjects), [Judgement](#judgement), [Lighting](#lighting), [Receptor](#receptor) and [Stage] folders.

### HitObjects
These are the files that determine how the notes themselves look. For easier readability between transitions, it's advised to have the multiple keymode skin elements match each other.
For these HitObjects, they're broken down into 3 more folders: [LongNoteBody](#longnotebody), [LongNoteEnd](#longnoteend), and [Note](#note).

##### LongNoteBody
This element is what is used for the middle of the Long Note. These are formatted as 4k-{x}.png, such as `4k-1.png` -> `4k-4.png`, and 7k-{x}.png, such as `7k-1.png` -> `7k-7.png`.

##### LongNoteEnd
This element is what is used for the end of the Long Note. These are formatted as 4k-{x}.png, such as `4k-1.png` -> `4k-4.png`, and 7k-{x}.png, such as `7k-1.png` -> `7k-7.png`.

##### Note
This element is what is used for both the start of the Long Note a. These are formatted as 4k-{x}.png, such as `4k-1.png` -> `4k-4.png`, and 7k-{x}.png, such as `7k-1.png` -> `7k-7.png`.

## Judgement
These are the files that determine what image shows up for each of the judgements hit in-game. 
These are labelled as `flawless.png` for the maximum hit judgement, `perfect.png` for the 300 judgement, `great.png` for the 200 judgement, `alright.png` for the 100 judgement, `okay.png` for the 50 judgement, and `miss.png` for the miss judgement.

## Lighting
This is what decides what image shows up when hitting each column. This is labelled as `column-lighting.png`.

## Receptor
This are the images that note where the columns are and were the judgement line should be at. The `down.png` images represent when the key is pressed, and the `up.png` images represent when the key is not pressed.

These files are formatted as the following:
- `1k-1-down.png`, `1k-1-up.png`
- `4k-1-down.png` -> `4k-4-down.png`, `4k-1-up.png` -> `4k-4-up.png`
- `5k-1-down.png` -> `5k-5-down.png`, `5k-1-up.png` -> `5k-5-up.png`
- `7k-1-down.png` -> `7k-7-down.png`, `7k-1-up.png` -> `7k-7-up.png`

## Stage
These decide how the non-playfield elements are rendered in game. These include `border-left.png` and `border-right.png` which decide how the left and right side of the playfield look like, and `hitline.png` which shows where the hitwindow is for notes.

## json
This is the code that makes the skin work. For each keymode, you can see the column width and the hitposition. It's advised to keep the values the same between keymodes so avoid awkward looking transitions. These values will also scale all of the above images, so try to get the image width to match the column width in the .json file to make editing and setting the hit position easier.

For each keymode, the format as follows (using 1K as an example):
`"1k": {`
`"column_width": 100,`
`"hit_position": 44`
`},`

`column_width` decides the width of each column in pixels, `hit_position` decides how many pixels up from the bottom of the screen the hit position is.
This goes from 1K to 10K so all keymodes will need to be added.

Also needed in the .json file is the judgement colour. These decide what colour the Judgement Splash is when displayed. These are handled in the following way:
`"judgements": {`
`"flawless": "#EAFFFC",`
`"perfect": "#FFCD4A",`
`"great": "#27F498",`
`"alright": "#0EB0B9",`
`"okay": "#808080",`
`"miss": "#F7314F"`
`}`

To get a template of a skin.json file, you will be able to download it here.