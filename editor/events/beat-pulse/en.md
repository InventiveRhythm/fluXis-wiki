# Beat Pulse

Not to be confused with [Pulse](/editor/events/pulse/).

Zooms the screen in periods set by beat intervals.

### Location
- Design Tab

## How Zoom in % Works

Beat Pulse does not have an easing parameter but, it uses ``OutQuint``.

Zoom in % essentially means how much of the **beginning** animation will be used, basically the first the half of the animation aka the initial zoom in/out. The other half is for reseting back to the original scale (1.0x).

### How `Zoom in %` Affects Animation

![Zoom in % at 0%](https://media.discordapp.net/attachments/1122621899487313920/1425150040187605054/zoom__0.png?ex=68e689e7&is=68e53867&hm=67fd5cf8c01e3460fe26c03cbf4cfa8664f1eeb6dade949aa8c38e0e739f1bb3&=&format=webp&quality=lossless&height=300&width=400)

![Zoom in % at 50%](https://media.discordapp.net/attachments/1122621899487313920/1425150040648712192/zoom__50.png?ex=68e689e7&is=68e53867&hm=7c8ad76fd52d493bcfe3a9dcf58d3d76ea921777fc1ebc12d4524aa5c179ec68&=&format=webp&quality=lossless&height=300&width=400)

## Considerations
- Negative strength inverts the screen vertically and horizontally and it will start from the normal scale to 0 to the negative value so, the screen will be at scale 0 for a moment.

## Properties

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| **Time** | `Decimal` | The start time of the event, in milliseconds. |
| **Strength** | `Decimal` | The strengh of the pulse effect aka how much to zoom. |
| **Zoom in %** | `Slider` | How much of the animation should be used for zooming. |
| **Interval** | `Decimal` | How many beats between each pulse. |

### Design
Event color: `#9973EF`
