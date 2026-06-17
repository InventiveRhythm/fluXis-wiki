# Timing Point

Timing Points define the rhythm of your chart, affecting timing and by relation how fast it is. Timing Points are the most essential event for all charts.

### Location
- Charting Tab

## Timing

### Bpm

Beats Per Minute (BPM) is the speed of the song. It defines how many beats occur in one minute. A higher BPM means the song is faster, resulting in beats that are closer together in time. A lower BPM means a slower song with beats that are further apart.

### Offset

Adding offset means beats occurs later.

Subtracting offset means beats occurs earlier.

### Time Signature

The Time Signature (e.g., 4/4, 3/4) defines the number of beats per measure. Most songs use a 4/4 time signature, meaning there are four beats in every measure. A 3/4 time signature would mean there are three beats per measure.

## Considerations

- When Changing Parameters, the notes placed will be desynced, a quick fix would be to go `Edit > Re-snap all notes`.

    Re-snapping notes will choose your current selected notes and beat-snap down next to the timeline, so make sure you select the appropiate notes and beat-snap before re-snapping.

    If you don't have notes selected it will re-snap  all notes present in the chart.

## Properties

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
| **Time** | `Decimal` | The start time of the event, in milliseconds. |
| **BPM** | `Decimal` | **Beats Per Minute**. Basically the song's speed; higher BPM means faster, closer-spaced beats. **Cannot** be negative or zero. |
| **Time Signature** | `Integer` | The number of beats per measure (e.g., 4/4, 3/4). Most songs use 4/4 time. **Cannot** be zero |
| **Hide Lines** | `Toggle` | Whether to show a Line every measure (every 4 beats). |

### Design
Event color: `#00FF80`

Tag color: `#00FF80`

## Trivia
- Setting the Time Signature to zero is possible but crashes the game. Even just viewing the map in song select crashes the game.