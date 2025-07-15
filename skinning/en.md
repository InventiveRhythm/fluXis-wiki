# Skinning

To begin skinning, go to Settings -> General -> Folders -> Open fluXis folder, or navigate to:

- Windows: `C:\Users\{username}\AppData\Roaming\fluXis\` 
- Linux: `~/.local/share/fluXis/` 

and create a folder named `skins`.

There are 8 different sections that go into each skin. The JSON file should be located at the root folder of your skin, while all of the other sections should be in their respective folders.

-   [Health](/wiki/skinning/health)
-   [HitObjects](/wiki/skinning/hitobjects)
-   [Judgement](/wiki/skinning/judgement)
-   [Lighting](/wiki/skinning/lighting)
-   [Receptor](/wiki/skinning/receptor)
-   [Samples](/wiki/skinning/samples)
-   [Stage](/wiki/skinning/stage)
-   [skin.json](/wiki/skinning/json)

Skins can also provide an icon for the skin selection menu. This icon should be a PNG file named `icon.png` and placed in the root folder of the skin.

Any images provided in the skin should NEVER exceed 4096x4096 pixels in size due to performance reasons.
