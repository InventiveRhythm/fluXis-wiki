# Skinning

To begin skinning, go to Settings -> General -> Folders -> Open fluXis folder, or navigate to:

- Windows: `C:\Users\{username}\AppData\Roaming\fluXis\` 
- Linux: `~/.local/share/fluXis/` 

and create a folder named `skins`.

## Creating a skin

Inside the `skins` folder, make another folder for your skin, and make a file named `skin.json` in that folder. More about skin.json can be found [here](/wiki/skinning/json).

Skins can also provide an icon for the skin selection menu. This icon should be a PNG file named `icon.png` and placed in the root folder of the skin.

Your `skins` folder should look like this:
```
skins
└── [Skin Name]
    ├── skin.json
    └── icon.png [optional]
```

> [!IMPORTANT]
> Any images provided in the skin should NEVER exceed 4096x4096 pixels in size due to performance reasons.

## Skin structure

There are 8 different sections that go into each skin, with their respective folders.

-   [Health](/wiki/skinning/health)
-   [HitObjects](/wiki/skinning/hitobjects)
-   [Judgement](/wiki/skinning/judgement)
-   [Lighting](/wiki/skinning/lighting)
-   [Receptor](/wiki/skinning/receptor)
-   [Samples](/wiki/skinning/samples)
-   [Stage](/wiki/skinning/stage)

To modify elements in that section, create a folder in the root of your skin with the name of that section.

For example, if you're skinning HitObjects and Lighting:
```
skins
└── [Skin Name]
    ├── [...]
    ├── HitObjects
    │   └── [...]
    └── Lighting
        └── [...]
```
