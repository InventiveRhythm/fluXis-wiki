# Scroll Velocity

> This page may be incomplete and might not be accurate.
>
> Things for wiki editors to consider:
> - Add explaination for sv gimmicks

Scroll Velocity, not to be confused with [Scroll Multiplier](/editor/events/scroll-multiplier/), multiplies the current scroll speed, changing its speed **before** the event time, meaning you can see its effect before triggering the event; Allowing for cool Gameplay gimmicks & visuals.

Can also be used with [Scroll Multiplier](/editor/events/scroll-multiplier/).

### Location
- Design Tab
- Charting Tab (As Tags)

## Multiplier

Multiplier Values ``< 1`` makes notes slower and closer to each other.

Multiplier Values ``> 1`` makes notes faster and spaced further from each other.

### Negative Multipliers

Negative multiplier values reverse the direction of the scroll.

Since they Reverse the direction of the scroll, they also offset the position of the notes appearing earlier,
However the [Time Offset](/editor/events/time-offset/) event is better suited for this.


## Properties

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| **Time** | `Decimal` | The start time of the event, in milliseconds. |
| **Multiplier** | `Decimal` | The speed to multiply scroll speed by. **Can** be negative or zero. |
| **Group** | `Toggle Boxes` | Also known as `Lane Masks`. Affects what lane it should apply the scroll velocity to |

### Design
Event color: `#00D4FF`

Tag color: `#00D4FF`
