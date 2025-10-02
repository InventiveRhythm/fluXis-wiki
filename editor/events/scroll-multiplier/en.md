# Scroll Mutliplier

> This page may be incomplete.
>
> Things for wiki editors to consider:
> - Add explaination for sv gimmicks

Scroll Mutliplier, not to be confused with [Scroll Velocity](/editor/events/scroll-velocity/), multiplies the current scroll speed across a period of time, changing its speed **after** the event time, meaning its effect triggers only after passing it, Unlike [Scroll Velocity](/editor/events/scroll-velocity/) where you can see its effect before reaching the event.

Can also be used with [Scroll Velocity](/editor/events/scroll-velocity/).

What makes Scroll Multiplier unique is that you can apply an easing function to have scroll speed change at different rates.

### Location
- Design Tab
- Charting Tab (As Tags)

## Multiplier

Multiplier Values ``< 1`` makes notes slower and closer to each other.

Multiplier Values ``> 1`` makes notes faster and spaced further from each other.

Negative multiplier values reverse the direction of the scroll.

## Properties

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| **Time** | `Decimal` | The start time of the event, in milliseconds. |
| **Animation Length** | `Decimal` | The duration of the animation, in beats. |
| **Multiplier** | `Decimal` | The speed to multiply scroll speed by. **Can** be negative or zero. |
| **Easing** | `Dropdown` | The easing function used to interpolate between multipliers. |
| **Group** | `Toggle Boxes` | Also known as `Lane Masks`. Affects what lane it should apply the scroll multiplier to |

### Design
Event color: `#c73673`

Tag color: `#c73673`
