# BIN Mappings BH
Less cursed Plasma Mappings, refactored for Beta Horizons project.

[![Jitpack](https://jitpack.io/v/paulevsGitch/BIN-Mappings-BH.svg)](https://jitpack.io/#paulevsGitch/BIN-Mappings-BH)

Project based on a BIN (Boring Instructive Names) mappings that are based on Plasma Mappings for Minecraft Beta 1.7.3.
The goal of this fork is to make mappins as complete as possible, fix errors in original mappings and change some names.

[Contributors and maintainers of original mappings](MAINTAINERS.md)

[Original Description](https://github.com/calmilamsy/BIN-Mappings/blob/master/README.md)

### Differences from original mappings:
- More mapped classes, fields and methods
- Changes in some packages
- Fixes for wrong names
- World -> Level name convertion
- Tile -> Block name convertion
- TileEntity -> BlockEntity name convertion
- TypeName -> NameType conversion (example BaseBlock -> BlockBase)
- Name -> NameType conversion (example Block -> BlockItem)

### To use this as a part of your gragle project:

1. Add jitpack to you repositories:

```
maven {
	name = 'Jitpack'
	url = 'https://jitpack.io'
}
```

2. Add this into dependencies (or replace existing mappings entry):

```
mappings "com.github.paulevsGitch:BIN-Mappings-BH:${project.mappings}"
```

3. Add version to your gradle.properties:

```
mappings = a504591
```
You can use any commit version here.