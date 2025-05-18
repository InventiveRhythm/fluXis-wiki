# .fsb (File format)
`.fsb`, like other file formats for fluXis charts use a JSON file format for human readability. Therefore, each key value MUST be made as a string (within quotes `""`). All positions, dimensions and times can use decimal values. (i.e. `"x": 12.235` is valid but `"layer": 2.222` is not valid)
NOTE: Keys that do not include a `Default` value will cause an error if not filled.
(i.e. Text sprites require a `text` parameter)
## Base
- `resolution` Base storyboard size (in pixels) that gets scaled to the users screen 
    - `x` / `y` - width and height of the base storyboard.
        - Default - `{x: 1920, y: 1080}`
- `elements` is a list of [[#Elements]] that appear through out the storyboard.
    - Default: `[]`
## Elements
- `type` - Type of element being created: 
    - `0` = `box` - Simple rectangular box.
    - `1` = `sprite` - A transformable image.
    - `2` =  `text` - Renders the default fluXis text sprite.
    - `3` = `script` - Runs a [[Lua Storyboard Scripting]] file for the effect.
- `start` - The time (in milliseconds) of the element being spawned. 
- `end` - The time (in milliseconds) of the element being de-spawned.
- `layer`:
    - `0` = `Background`
    - `1` = `Foreground`
    - `2` = `Overlay` - Displays the sprite on top of the playfield.
        - Default - `0`
- `width` - The width of the element. (only applies to `box` elements)
    - Default: `0.0`
- `height` - The height of the element. (only applies to `box` elements)
    - Default: `0.0`
- `anchor`- A [bitflag](https://en.wiktionary.org/wiki/bitflag) value of how the anchor (position relative to on the playfield) is positioned. List of values found at [osu!framework's Drawable class](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable.cs#L2715)
    - Default: `0` - TopLeft
- `origin` - A [bitflag](https://en.wiktionary.org/wiki/bitflag) value of how the origin (on element) is positioned. List of values found at [osu!framework's Drawable class](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable.cs#L2715)
    - Default: `0` - TopLeft
- `z-index` - The absolute position (without decimals) within the layer above or below other elements.
    - Default: `0`
- `x` - X Position of the sprite relative to the anchor.
    - Default: `0.0`
- `y` - Y Position of the sprite relative to the anchor.
    - Default: `0.0`
- `parameters` - See [[#Parameters]]
- `animations` - See [[#Animations]]
    - Default: `[]`

## Parameters
Parameters are different depending on the element type being created.
### Box
- As the width and height are set in the element itself. No additional parameters are required.
### Sprite
- `file` - A Relative file path to an image (with extension, fluXis supports `.jpg`, `.jpeg` and `.png`) to be used as a sprite.
NOTE: Take into account that Purifying Criteria applies to ALL image sprites, not just the background and cover sprites.
### Text
- `text` - The text to be displayed as a string (within quotes)
- `size` - The Font size (in units)
    - Default: `20`
### Script
- `path` - Relative path to the [[Lua Storyboard Scripting]] file (including extension)

## Animations
Animations are a list of simple keyframes that can transform your element throughout the storyboard.
- `start` - Time (in milliseconds) for the keyframe animation to start in the chart.
- `duration` - Time relative to the `start` value (in milliseconds) for the keyframe animation to end.
- `easing` - An enum value (as an integer, no decimals) for the keyframe easing. See the [osu! wiki page](https://osu.ppy.sh/wiki/en/Storyboard/Scripting/Commands)  for a list of easing values and their integer values.
    - Default: `0` - None
- `type`:
    - `0` - Move X -Translates the element in the X axis.
    - `1` - Move Y - Translates the element in the Y axis.
    - `2` - Scale - Scales the element uniformly across both horizontal and vertical axis.
    - `3` - Vector Scale - Scales the element independently of both horizontal and vertical axis.
        - Note: the `start-value` and `end-value` changes format when this type is used. See [[#Values]] for more info.
    - `4` - Width - Changes the width of the element (only affects `box` elements)
    - `5` - Height - Changes the height of the element (only affects `box` elements)
    - `6` - Rotate - Rotates the element (in degrees)
    - `7` - Fade - Changes opacity of the element (`0` - no opacity, `1` - full opacity)
    - `8` - Color - Changes color of the element
        - Note: the `start-value` and `end-value` changes format when this type is used. See [[#Values]] for more info.
- `start-value` - See [[#Values]]
- `end-value` - See [[#Values]]
#### Values
`start-value` and `end-value` define how the element would behave from `start` to the end of it's keyframe.
Most cases use numbers (with/without decimals) with some exceptions.
- `Vector Scale` uses a width and height value used as a string (within quotes `""`) separated with a comma (`,`)
    - Example: `4,10` scales the element by 4x for the width and 10x for the height.
- `Color` uses a uint (positive real number) representation of the RRGGBBAA value. (This value uses a different value when using [[Lua Storyboard Scripting]])
    - Default: `4294967295` - `0xFFFFFFFF`
# Example
Example storyboard (prettified) including a sprite fade in and a script definition:
```
{
    "resolution": {
        "x": 1920.0,
        "y": 1080.0
    },
    "elements": [
        {
            "type": 1,
            "layer": 0,
            "z-index": 0,
            "start": 760.0,
            "end": 95927.0,
            "anchor": 18,
            "origin": 18,
            "x": 0.0,
            "y": 0.0,
            "width": 0.0,
            "height": 0.0,
            "color": 4294967295,
            "parameters": {
                "file": "sb\\IMG_0265.jpg"
            },
            "animations": [
                {
                    "start": 760.0,
                    "duration": 10000.0,
                    "easing": 2,
                    "type": 7,
                    "start-value": "0",
                    "end-value": "1"
                }
            ]
        },
        {
            "type": 3,
            "layer": 2,
            "z-index": 0,
            "start": 57860.0,
            "end": 95927.0,
            "anchor": 18,
            "origin": 18,
            "x": 0.0,
            "y": 0.0,
            "width": 1920.0,
            "height": 1080.0,
            "color": 4294967295,
            "parameters": {
                "path": "rain-particles.lua"
            },
            "animations": []
        }
    ]
}
```

