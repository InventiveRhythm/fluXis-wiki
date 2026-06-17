# Playfield Rotate

Allows for rotating all Playfields or specific Playfields around their origins (playfield center).

### Location
- Design Tab

## Considerations

- Since all subfields start as invisible, when changing values for other playfields make sure you have them visible via [Layer Fade](/editor/events/layer-fade/).

- Rotations are absolute not relative. When you set a rotation value, the playfield rotates to that exact angle.

    **Example:**
    - If the playfield is currently at 360°, setting the rotation to 30° will cause it to rotate from 360° to 30°
    - Each ``Playfield Rotate`` event sets the absolute angle, not an offset from the current rotation.

## Properties

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| **Time** | `Decimal` | The start time of the event, in milliseconds. |
| **Animation Length** | `Decimal` | The duration of the animation, in beats. |
| **Rotation** | `Decimal` | Rotate around playfield's center, in degrees. |
| **Easing** | `Dropdown` | The easing function used to interpolate between rotations. |
| **Player Index** | `Slider` | What Player to apply this event to (Only available in dual mode). |
| **Subfield Index** | `Slider` | What playfield should this event be applied to. |

### Design
Event color: `#8AF7A2`
