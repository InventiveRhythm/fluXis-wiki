# Shader

> This page may be incomplete.
>
> Things for wiki editors to consider:
> - Better explaination

A special event that applies a fragment shader to the screen.
Shaders are a fun way to upgrade a map's visuals.

### Location
- Design Tab

## Properties

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| **Time** | `Decimal` | The start time of the event, in milliseconds. |
| **Animation Length** | `Decimal` | The duration of the animation, in beats. |
| **Shader** | `Dropdown` | The shader to be applied to the screen. |
| **Use Start Value** | `Toggle` | Enables whether start strength value should be used. |
| **Start Strengh** | `Slider` | what strength the shader starts at. |
| **End Strengh** | `Slider` | what strength the shader ends at. When `Use Start Value` is off it will be interpolated to from the previous event. |
| **Easing** | `Dropdown` | The easing function used to interpolate between start and end values. |

### Design
Event color: `#D65C5C`

## Trivia
- `Glitch` and `Reflections` are the most used shaders, often overused.
