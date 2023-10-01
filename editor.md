# Editor

## Accessing the Editor

To open the Editor to begin editing a new map, simply click the Edit button found on the homepage.

To open the Editor to edit an existing map, find the mapset in the Song Select screen, open it and find the map, and Right Click -> Edit.

## Setup

To begin creating the map, you first need to fill out all of the important information about the map.

To add audio, click on Audio and choose the audio file you wish to use. The formats that are acceptable to use are .mp3, .wav, and .ogg.

To add a background, click on Background and choose the background image you wish to use. Any .jpg and .png file should be supported.

A cover is used to represent the icon of the map in Song Select. To add a cover, click on Cover and choose the cover image you wish to use. Any .jpg and .png are supported but an image close to a square shape is preferred.

Videos can also be added to maps, the supported formats are: .mp4, .mov, .avi, .flv, .mpg, .wmv, and .m4v. These can be added by clicking Video, and then choosing the video you wish to use.

For Metadata, make sure to add the Title of the song, the Artist, yourself as the Mapper, and also give it a difficulty name under Difficulty. Sources should also be included if there are any. Make sure to include all sources separated with commas. Additionally, add tags to make your map more searchable in the Mapset Listing.

Lastly, for Keys, choose the maximum keymode you wish to use for the map. If you're planning to use 1K - 8K, select 8 Keys.

## Timing

To set timings correctly in the editor, it helps by having View -> Waveform opacity set to at least 25%.

The first thing to set in terms of timing will be the offset. In the Charting Panel, scroll through the map until you find the first big line in the waveform. This should align with the first big drum beat in the song (if the song has a drum beat), so validate the waveform against the song where possible. 

Once you've found the start of the song, take a note of where you are in the timeline at the bottom left. If it's not perfectly aligned, don't worry, we can make adjustments to it later. Go back to the Timing Panel and set the first Timing Point to match the offset you noted. Now, if you need to adjust further, increase the offset values if the first beat is vertically higher than the current offset, and decrease the offset values if the first beat is vertically lower than the current offset until you find the right place.

Now, in terms of setting the BPM, when listening to the song, see if the overall beat of the lines (represented by the white lines) are either ahead or behind the beat of the song. If the white lines are behind the beat of the song, increase the BPM until they match. If the white lines are ahead of the beat of the song, decrease the BPM until they match.

## Charting

Now that the map is setup, it's time to begin placing notes. Usually for most songs you'll find that the beats will line up on the 1/4 beat snaps, denoted by the red and blue lines. If you ever need to change the snap, hold down Shift and then scroll the mouse wheel. You can also zoom out the editor by holding down Ctrl and also scroll the mouse wheel.

In terms of gameplay changes, you have five options available. Selecting and Moving objects, Placing a Single Note, Placing a Long Note, Adding a Lane Switch, and Adding a Flash.

The Select tool will allow you to select either a solo note or a group of notes together, and allow you to move them around the playfield, either between different columns or to different snaps.

The Single Note tool allows you to place a single note onto the playfield depending on when you place the cursor. You will see a note preview on the playfield where the note will be placed, so you can see exactly what column and what snap the note will go in before clicking. Also, right clicking will delete the note underneath the cursor.

The Long Note tool allows you to place a long note onto the playfield depending on where you click and drag the cursor. If the cursor isn't dragged to at least one snap above or below, it will create a single note instead. The long note will match the length of the nearest snap to the cursor when you release. Once placed, long notes cannot be adjusted in length, so you can right click to delete the note and try again.

The Lane Switch effect is the main feature of this game, and allows the mapper to change the keymode the mapper is in. To apply this to the map, select the tool, and then drag from the left to right at the snap you want to apply the change in to decide the keys you want. Placing it far left will reduce the playfield down to 1K, and placing it far right will extend the playfield to the maximum keymode selected earlier. 

Once placed, you can use the Select Tool to edit the Lane Switch options. Clicking on an empty part of the playfield will open up the Lane Switch options for that section and give you three options. The Time sets the start time of the Lane Switch. The Speed decides how many beats after the initial time set will it take to complete the transition between keymodes. The Lanes decide how many columns will be available after the switch is completed. If you wish to delete the switch, just press Delete.

The Flash effect allows the mapper to put in an effect that changes the full screen to be a certain colour for a customisable amount of time. To apply this, select the tool, click where you want to start, and drag to decide the effect's length. To edit this further, click the flash effect on the right side of the field to open the Flash Editor.

The Flash Editor allows for precise editing on how the flash is displayed to the user. The Time denotes the start time of the flash. The Duration decides how many beats the flash lasts. The Start Color allows the mapper to set the immediate colour displayed at the beginning of the flash, and the Start Opacity sets the visibility of the flash at the beginning. Likewise, the End Color and End Opacity sets the colour that the flash will transition into, and the opacity will set the visibility that the flash will transition into. To delete the effect entirely, just press Delete.

## Other Features

The Timeline at the bottom of the screen displays all the useful information, like current progress through the song, the BPM, and the BPM placements in the timeline. You can also slowdown the map speed, and test the map with the Test! button at the bottom right.

The Timing menu option at the top allows you to set the preview point, where the song starts playing in the Song Select menu.

The View menu allows you to set the waveform opacity in the editor, as well as set the visibility of the flash effect bar on the right side of the field, as well as deciding if the bar is light or dark.

The Edit menu allows you to Undo and Redo edits to the map, Cut/Copy/Paste/Delete notes, as well as being able to Select All notes.

The File menu allows you to Save the map (can also be done with Ctrl-S), as well as Exporting the map to share, and Upload the map to the fluxis servers to link to others and apply for ranking. You can also open the song folder to get access to the map's files, allowing editing of the notes file (.fsc) and effects file (.ffx). Please be cautionary when editing these files as any damage done to them will cause the map to fail to load.

Go to File -> Exit or hit ESC on the keyboard to leave the editor.