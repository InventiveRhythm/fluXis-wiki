# Playfield Move

Allows for moving all Playfields or specific Playfields.

## Considerations

- Since all subfields start as invisible, when changing values for other playfields make sure you have them visible via [Layer Fade](/editor/events/layer-fade/).

## Properties

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| **Time** | `Decimal` | The start time of the event, in milliseconds. |
| **Animation Length** | `Decimal` | The duration of the animation, in beats. |
| **Offset X** | `Decimal` | Move Horizontally to this axis |
| **Offset Y** | `Decimal` | Move Vertically to this axis |
| **Offset Z** | `Decimal` | The Depth of the Playfield (basically size) |
| **Easing** | `Dropdown` | The easing function used to interpolate between positions. |
| **Player Index** | `Slider` | What Player to apply this event to (Only available in dual mode). |
| **Subfield Index** | `Slider` | What playfield should this event be applied to. |

### Design
Event color: `#01FE55`
