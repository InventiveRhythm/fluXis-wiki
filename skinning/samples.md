# Samples

You can customize the sounds for when a key is pressed, you miss a note, etc.

|Sample|Usage|
|---|---|
|`fail.wav`|Failing for any reason.|
|`hit.wav`|Pressing a key.|
|`miss.wav`|Missing notes|
|`restart.wav`|Restarting the game either via the pause menu or quick retry|

You can have multiple miss sounds, and the game will randomly pick one among all the samples you have put. Make sure the first four letters are "miss" in the file name, and whatever comes after will be ignored.

- Names like `miss test.wav`, `misster.wav`, `miss-alt.wav`, and `missssssss.wav` will work.
- Names like `another miss.wav`, `mis.wav`, and `mis1.wav` will **not** work