# Conventions:

## These conventions are likely to change a fair bit during mapping, so be sure to check back to make sure nothing has changed.

1. Use British English.

2. Use concise names where it is sensible. (e.g: `net.minecraft.entity.Creeper` instead of `EntityCreeper`)

    2a. If a class extends a built-in java class (e.g: `SessionValidator` becomes `ThreadSessionValidator`)

    2b. If a class is generally only used for other classes to extend, append `Base` to the end. (e.g: `Item` becomes `ItemBase`)

    2c. If a class is for rendering, it should have `Renderer` appended. (e.g: `Wolf` becomes `WolfRenderer`)

    2d. If a class is an interface, append `I` to the start. (e.g: `Block` becomes `IBlock`)

    2e. `World` (in MCP) should be called `Level` instead. (e.g: `WorldRenderer` becomes `LevelRenderer`)

3. Use sensible, MCP-esque names.

4. Everything should be in a suitibly named package. (e.g: `Creeper` belongs in `net.minecraft.entity.mob`, `ItemBed` belongs in `net.minecraft.item`)

    4a. If a class inherits a minecraft class and has `Base` appended, it belongs in the package of the class it inherits from. Exception if a class is different enough to warrant a new package for it.