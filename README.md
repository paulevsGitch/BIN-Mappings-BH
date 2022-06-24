# BIN Mappings
## Less cursed Plasma Mappings

BIN (Boring Instructive Names) is a set of less cursed Plasma Mappings for beta 1.7.3.

The Gradle used for this is mostly still based of Yarn's, so improvements to the Gradle tasks are welcome.

[Maintainers](MAINTAINERS.md)

## Usage
To use yarn-deobfuscated Minecraft for Minecraft modding or as a dependency in a Java project, you can use [loom](https://github.com/fabricmc/fabric-loom) Gradle plugin. See [fabric wiki tutorial](https://fabricmc.net/wiki/tutorial:setup) for more information.

To obtain a deobfuscated Minecraft jar, [`./gradlew mapNamedJar`](#mapNamedJar) will generate a jar named like `<minecraft version>-named.jar`, which can be sent to a decompiler for deobfuscated code.
Alternatively, use the functions provided by enigma to decompile

### Making a Mod

You will want to use [BIN Example Mod](https://github.com/calmilamsy/BIN-fabric-example-mod).

### Using a Mod

You will want to use the [Cursed Fabric MultiMC Instance](https://github.com/calmilamsy/Cursed-Fabric-MultiMC)

## Contributing

Please remember that copying and pasting mappings from alternate projects under more restrictive licenses (such as the real MCP) is **completely forbidden** without explicit permission from the 
owners of said mappings.

When contributing remember to [read the conventions](CONVENTIONS.md).

To contribute, fork the project and clone it locally, and use  Enigma to map the jar. Then push to your fork and submit a pull request.

**Anyone** can comment and suggest changes on pull requests. We want to make sure the mappings are the best quality, so make your voice known!

# Getting Started

MCPomf (now Plasma) started as a yarn fork, so tasks currently still reference yarn.

1. Fork and clone the repo
2. Run `./gradlew yarn` (Linux, macOS) or `.\gradlew yarn` (Windows)
3. Profit

## Gradle
This uses Gradle to provide a number of utility tasks for working with the mappings.

### `yarn`
Runs [`setupYarn`](#setupYarn) and downloads and launches the latest version of Fabric's fork of [Enigma](https://github.com/FabricMC/Enigma) with the mappings and jars pre-loaded for editing.

Compared to launching Enigma externally, the gradle task adds a name guesser plugin that automatically map enums and a few constant field names.

### `build`
Build a GZip'd archive containing a tiny mapping between official (obfuscated), [intermediary](https://github.com/FabricMC/intermediary), and MCPomf names ("named") and packages enigma mappings into a zip archive..

### `mapNamedJar`
Builds a deobfuscated jar with yarn mappings and automapped fields (enums, etc.).

### `download`
Downloads the client and server Minecraft jars for the current Minecraft version to `.gradle/minecraft`

### `setupYarn`
Runs [`download`](#download) and does some things to make yarn work.