# Time Offset

> This page may be incomplete.
>
> Things for wiki editors to consider:
> - Add explaination for sv gimmicks

Time Offset allows you to offset the notes' (visual) position, meaning their hit timings stay unaffected. This event makes it easier to change the position of the notes without having to rely on [Scroll Velocity](/editor/events/scroll-velocity/).
However, Time Offset is only triggered after passing the event's time Unlike [Scroll Velocity](/editor/events/scroll-velocity/) where you can see the its effect before the event time so, it's not a total replacement for note position manipulation.

### Location
- Design Tab

## Difference between Time Offset & Scroll Events

Time Offset differs from [Scroll Multiplier](/editor/events/scroll-multiplier/) & [Scroll Velocity](/editor/events/scroll-velocity/) in that it doesn't affect the spacing of the notes.

## Offset

Offset ``< 0`` makes notes appear later & is hit earlier.

Offset ``> 0`` makes notes appear earlier & is hit later.

## Properties

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| **Time** | `Decimal` | The start time of the event, in milliseconds. |
| **Animation Length** | `Decimal` | The duration of the animation, in beats. |
| **Use Start Value** | `Toggle` | Enables whether start offset value should be used. |
| **Start Offset** | `Decimal` | The starting visual offset, in beats. |
| **Target Offset** | `Decimal` | The target visual offset, in beats. |
| **Easing** | `Dropdown` | The easing function used to interpolate between start and end values. |

### Design
Event color: `#fa8ca1`
