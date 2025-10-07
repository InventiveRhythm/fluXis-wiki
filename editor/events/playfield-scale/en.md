# Playfield Scale

Allows for scaling all Playfields or specific Playfields, either horizontally and/or vertically.

### Location
- Design Tab

## Considerations

- Since all subfields start as invisible, when changing values for other playfields make sure you have them visible via [Layer Fade](/editor/events/layer-fade/).

## Other Uses

Setting Scales to negative values inverts them. Sometimes used to flip playfield vertically by setting `ScaleY` to a negative value.

## Properties

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| **Time** | `Decimal` | The start time of the event, in milliseconds. |
| **Animation Length** | `Decimal` | The duration of the animation, in beats. |
| **ScaleX** | `Decimal` | The Horizontal scale multiplier. |
| **ScaleY** | `Decimal` | The Vertical scale multiplier. |
| **Easing** | `Dropdown` | The easing function used to interpolate between scales. |
| **Player Index** | `Slider` | What Player to apply this event to (Only available in dual mode). |
| **Subfield Index** | `Slider` | What playfield should this event be applied to. |

### Design
Event color: `#D279C4`
