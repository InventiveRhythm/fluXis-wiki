# Stage
These decide how the non-playfield elements are rendered in game. These include `border-left.png` and `border-right.png` which decide how the left and right side of the playfield look like, and `hitline.png` which shows where the hitwindow is for notes.

## Health
Images for the health bar are stored in `Health/`. Whenever you run out of health, a cross will appear in the middle of the health bar to indicate a loss.

It is recommended to keep the images the same size as `background.png` will define the dimensions of your healthbar, and `foreground.png` will be cropped to fit those dimensions. If `foreground.png` has smaller dimensions, the game will scale the image to fit the width. If the height is smaller than `background.png` after this, the game will scale up the image to match the level of the health bar.