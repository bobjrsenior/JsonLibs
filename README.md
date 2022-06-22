# JsonLibs

A simple BepInEx Il2CPP wrapper plugin for System.Text.Json and it's dependencies.

## Intallation

### Installing BepInEx

This plugin uses [BepInEx](https://github.com/BepInEx/BepInEx) as a mod loader so that needs to be installed first.

1. Download a bleeding edge build of "BepInEx Unity IL2CPP for Windows x64 games" [here](https://builds.bepinex.dev/projects/bepinex_be) (Only the bleeding edge builds support Il2CPP games)
2. Extract it in your game folder)

## Installing This Plugin

1. Download the JsonLibs.zip file from the Releases page
2. Extract it in your main game folder (the zip file structure should put the plugin in the right place)

## Plugin Contents

Here is what the plugin resources should look like:

```
JsonLibs/
├── JsonLibs.dll
├── LICENSE
├── Microsoft.Bcl.AsyncInterfaces.dll
├── System.Buffers.dll
├── System.Memory.dll
├── System.Numerics.Vectors.dll
├── System.Runtime.CompilerServices.Unsafe.dll
├── System.Text.Encodings.Web.dll
├── System.Text.Json.dll
└── System.Threading.Tasks.Extensions.dll
```

## Building

## Setup

I use Visual Studio 2022  for development although I beleive it can also be compiled via command line. Additionally, make sure you setup your enviroment for BepInEx plugin development: https://docs.bepinex.dev/master/articles/dev_guide/plugin_tutorial/1_setup.html

## Post-build event

The project includes Post-build events that will automatically copy the plugin into "$(SMBBMDir)\BepInEx\plugins". That way you can immediately run the game after building is complete for testing.

For the Post-buid event to work, you need to edit the `<SMBBMDir>` element in the .csproj. You can point it to your game installation to make it work.
