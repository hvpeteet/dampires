# Dampires (The Dam-ed)
WIP repo for a mod around the Dampires in Timberborn. Based on the mechanistry timberborn-modding repo.

## Basic process

1. Find an example of what you want in the ripped assets
2. Copy and edit the assets you care about into your mod
3. Use unity menu timberborn --> Show Mod Builder --> Build
   * Using the "Run the game after successful build"

## Basic mod structure (before being built)
```
repo_root
   Assets
      Mods
         YOUR_MOD_HERE
            AssetBundles
               FilesToBundle...
            Blueprints
               FileNameFromRippedAssetExtensionReplacedWithJSON.json
            Localizations
               enUS_YOUR_MOD_HERE.txt
            Materials
            Sprites
            manifest.json
```

All assets under AssetBundles will be magically bundled, they need to match the ripped assets structure, e.g.

```
repo_root
   Assets
      Mods
         YOUR_MOD_HERE
            AssetBundles
                Resources
                    Materials
                    ...
```

## Basic mod structure (once built)
When working on a Timberborn mod, you store it in the `Documents/Timberborn/Mods` directory, with each mod having its own subfolder. That is also where you store mods that you downloaded manually.

Example:
```
Documents/
└── Timberborn/
    └── Mods/
        └── MyFirstMod/
            ├── AssetBundles/
            │   └── ModAssets.assets
            ├── Blueprints/
            │   ├── Goods/
            │   │   ├── Good.Berries.json
            │   │   └── Good.Moonshine.json
            │   └── Recipes/
            │       └── Recipe.Antidote.json
            ├── Localizations/
            │   └── enUS_myMod.csv
            ├── Materials/
            │   └── Beavers/
            │       └── Folktails/
            │           └── Adult/
            │               ├── BeaverAdult1.Folktails.png
            │               ├── BeaverAdult2.Folktails.png
            │               └── BeaverAdult3.Folktails.png
            ├── Sprites/
            │   └── Goods/
            │       ├── MoonshineIcon.png
            │       └── MoonshineIcon.png.meta.json
            ├── Code.dll
            └── manifest.json
```
