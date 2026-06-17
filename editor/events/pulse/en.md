# Pulse

Not to be confused with [Beat Pulse](/editor/events/beat-pulse/).

Expands a white border around the edges of the screen.

### Location
- Design Tab

## How In % Works

In % essentially means how much of the **beginning** animation will be used, basically the first the half of the animation aka the initial expansion. The other half is for reseting back to the original width (0px).

### How `In %` Affects Animation

#### Easing in Examples

![In % at 0% (in)](https://media.discordapp.net/attachments/1122621899487313920/1425160154382336130/in_in__0.png?ex=68e69353&is=68e541d3&hm=87df8b216c5d6ab98c44b0b32c645954fe75ff4555c011f87efe52ceefdb97f2&=&format=webp&quality=lossless&height=300&width=400) ![In % at 50% (in)](https://media.discordapp.net/attachments/1122621899487313920/1425160151584866494/in_in__50.png?ex=68e69352&is=68e541d2&hm=d27b630f1973c6210385783e5e6e9392720ca3fcbe4bd7486a01c0b93ab144cf&=&format=webp&quality=lossless&height=300&width=400)

#### Easing out Examples

![In % at 0% (out)](https://media.discordapp.net/attachments/1122621899487313920/1425160153178574889/out_in__0.png?ex=68e69352&is=68e541d2&hm=7be8ad77beabd6739285fbf667695f0f0ea358415235e8fd51b3bac50cdc319c&=&format=webp&quality=lossless&height=300&width=400) ![In % at 50% (out)](https://media.discordapp.net/attachments/1122621899487313920/1425160152570658826/out_in__50.png?ex=68e69352&is=68e541d2&hm=eb53b1a9d194e58cfc7a1fd54cd461fa78a08bf5781a7736217fd16ad363fd21&=&format=webp&quality=lossless&height=300&width=400)

## Properties

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| **Time** | `Decimal` | The start time of the event, in milliseconds. |
| **Animation Length** | `Decimal` | The duration of the animation, in beats. |
| **Width** | `Slider` | The width of the expanded border. |
| **In %** | `Slider` | How much of the animation should be used for expanding. |
| **Easing** | `Dropdown` | The easing function used to interpolate between widths. |

### Design
Event color: `#F0F975`
