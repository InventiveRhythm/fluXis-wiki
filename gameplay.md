# Gameplay

## Main gameplay

fluXis is a Vertical Scrolling Rhythm Game with added extra visual features.

When playing a map you have to navigate through a vertically scrolling field with notes and press keys corresponding to notes that fall. The notes are synced to a music beat, so you have to use your sense of rhythm to hit them!

The game judges how accurately you hit the notes and calculates your score based on that.

## Accuracy

The accuracy with which you hit notes is based on the amount of judgements you acquire while playing the map. Following formula calculates accuracy:

```cs
int totalNotes = Flawless + Perfect + Great + Alright + Okay + Miss;
float ratedNotes = Flawless + Perfect * 0.98f + Great * 0.65f + Alright * 0.25f + Okay * 0.1f;
float accuracy = ratedNotes / totalNotes * 100;
```
## Judgement timing windows

fluXis has following timing windows for each judgement:
 
| Judgement | Hit Timing | Release Timing |
| --------- | ----------------------- | ----------- |
| ![](https://singlecolorimage.com/get/00C3FF/10x10) Flawless | ±16ms  | ±40ms  |
| ![](https://singlecolorimage.com/get/22FFB5/10x10) Perfect  | ±40ms  | ±73ms  |
| ![](https://singlecolorimage.com/get/4BFF3B/10x10) Great    | ±73ms  | ±103ms |
| ![](https://singlecolorimage.com/get/FFF12B/10x10) Alright  | ±103ms | ±127ms |
| ![](https://singlecolorimage.com/get/F7AD40/10x10) Okay     | ±127ms | ------ |
| ![](https://singlecolorimage.com/get/FF5555/10x10) Miss     | ±164ms | ------ |

*If you release a long note too early or late, it will be judged as alright.*

## Scoring system

This is how score is calculated:

```
private int getScore()
{
    var scoreMultiplier = 1f + Mods.Sum(mod => mod.ScoreMultiplier - 1f);
    
    var maxScore = 1000000 * scoreMultiplier;
    var accBased = (int)(ratedNotes / MapInfo.MaxCombo * (maxScore * .9f));
    var comboBased = (int)(MaxCombo / (float)MapInfo.MaxCombo * (maxScore * .1f));
    return accBased + comboBased;
}
```