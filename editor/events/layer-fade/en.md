# Layer Fade

Allows changing the opacity of certain layers during gameplay.

## Layers

- Hitobjects
- Stage
- Receptors
- Playfield
- HUD

## Properties

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| **Time** | `Decimal` | The start time of the event, in milliseconds. |
| **Animation Length** | `Decimal` | The duration of the animation, in beats. |
| **Alpha** | `Slider` | The opacity of the Layer. |
| **Easing** | `Dropdown` | The easing function used to interpolate between alphas. |
| **Layer** | `Dropdown` | The Layer to adjust the opacity of. |
| **Player Index** | `Slider` | What Player to apply this event to (Only available when Layer selected is `Playfield` and in dual mode). |
| **Subfield Index** | `Slider` | What Playfield should this event be applied to (Only available when Layer selected is `Playfield`). |

### Design
Event color: `#8AF3F7`
