# skin.json
This is the code that makes the skin work. For each keymode, you can see the column width, the hit position, and the column lighting tints.

For each keymode, the format is as follows (using 7K as an example):

```json
"7k": {
  "column_width": 80,
  "hit_position": 144,
  "colors": [
    "#f7314f",
    "#e85a5a",
    "#f7314f",
    "#dcc784",
    "#f7314f",
    "#e85a5a",
    "#f7314f"
  ]
}
```

- `column_width` decides the width of all the columns in pixels.
- `hit_position` decides how many pixels up from the bottom of the screen the hit position is.
- `colors` tints the hit lighting of each individual column. The first entry will tint the lighting in the first lane from the left of the stage, the second entry will tint the second lane, and so on.

This goes from 4K to 8K so these keymodes will need to be added. You can optionally include the other keymodes, but these are not required.

It's advised to keep the values the same between keymodes to avoid awkward looking transitions. These values will also scale all of the above images, so try to get the image width to match the column width in the .json file to make editing and setting the hit position easier.

### Judgement Colours
Also needed in the .json file are the judgement colours. These decide what colour the Judgement Splash is when displayed.

The default colours for each judgement are as follows:

|Judgement|Colour|
|---|---|
|Flawless|![](https://singlecolorimage.com/get/00C3FF/10x10) #00C3FF|
|Perfect|![](https://singlecolorimage.com/get/22ffb5/10x10) #22FFB5|
|Great|![](https://singlecolorimage.com/get/4bff3b/10x10) #4BFF3B|
|Alright|![](https://singlecolorimage.com/get/fff12b/10x10) #FFF12B|
|Okay|![](https://singlecolorimage.com/get/f7ad40/10x10) #F7AD40|
|Miss|![](https://singlecolorimage.com/get/ff5555/10x10) #FF5555|

### Overrides
Overrides allow you to set a different path for your elements, or use a single image in multiple elements. This helps with saving storage space as you don't have to use a duplicate image for a different element.

To add an override, provide the path relative to the root of your skin folder to the element you want to replace in the first option, and the path for what that element's going to replace it in the second option. Make sure not to put the file extensions in any of the options. The override won't work if you do.

Here's an example that will replace the Note in the first lane of a 4-key stage with an image named `note-1` in the `HitObjects` folder:

```json
"overrides": {
    "HitObjects/Note/4k-1": "HitObjects/note-1"
}
```

You can add more overrides to replace or consolidate elements as you see fit.

### Template
A general template of the entire `skin.json` is laid out for convenience.
```json
{
  "1k": {
    "column_width": 132,
    "hit_position": 130,
    "colors": []
  },
  "2k": {
    "column_width": 126,
    "hit_position": 130,
    "colors": []
  },
  "3k": {
    "column_width": 120,
    "hit_position": 130,
    "colors": []
  },
  "4k": {
    "column_width": 114,
    "hit_position": 130,
    "colors": []
  },
  "5k": {
    "column_width": 108,
    "hit_position": 130,
    "colors": []
  },
  "6k": {
    "column_width": 102,
    "hit_position": 130,
    "colors": []
  },
  "7k": {
    "column_width": 96,
    "hit_position": 130,
    "colors": []
  },
  "8k": {
    "column_width": 90,
    "hit_position": 130,
    "colors": []
  },
  "9k": {
    "column_width": 84,
    "hit_position": 130,
    "colors": []
  },
  "10k": {
    "column_width": 78,
    "hit_position": 130,
    "colors": []
  },
  "judgements": {
    "flawless": "#00C3FF",
    "perfect": "#22FFB5",
    "great": "#4BFF3B",
    "alright": "#FFF12B",
    "okay": "#F7AD40",
    "miss": "#FF5555"
  },
  "overrides": {}
}
```