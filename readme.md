# Description

A generic mod based on my [MagicLoaderGenerator](https://github.com/North-Edge/MagicLoaderGenerator) library that will automatically translate any [MagicLoader](https://www.nexusmods.com/oblivionremastered/mods/1966?tab=description) files placed in its `Input` directory and generate an archive per language. Requires the game translation files to be placed in the `Localization` directory.

Change the **ModName** in **config.json** to match the name you want for the generated archives.

Mods created using the [MagicLoaderGenerator](https://github.com/North-Edge/MagicLoaderGenerator) library ([GitHub](https://github.com/North-Edge/MagicLoaderGenerator)) ([NuGet](https://www.nuget.org/packages/NorthEdge.MagicLoaderGenerator/)):

- [Mark Quest Dungeons - MagicLoader Edition](https://www.nexusmods.com/oblivionremastered/mods/3637) ([GitHub](https://github.com/Xebeth/MarkQuestDungeonsML))
- [Looted Soul Gems Content](https://www.nexusmods.com/oblivionremastered/mods/3831) ([GitHub](https://github.com/Xebeth/SoulGemsContentML) )
- this utility ([GitHub](https://github.com/Xebeth/GenericModTranslatorML) )


.NET Solution and Console project template are available to rapidly create similar mods ([GitHub](https://github.com/North-Edge/MagicLoaderGeneratorTemplates)) ([NuGet](https://www.nuget.org/packages/NorthEdge.MagicLoaderGenerator.Templates/)).

The structure of the project should look as follows:
```
+ GenericModTranslator
¦    config.json
¦    GenericModTranslator.deps.json
¦    GenericModTranslator.dll
¦    GenericModTranslator.exe
¦    GenericModTranslator.runtimeconfig.json
¦    MagicLoaderGenerator.dll
¦    Microsoft.Extensions.Configuration.Abstractions.dll
¦    Microsoft.Extensions.Configuration.Binder.dll
¦    Microsoft.Extensions.Configuration.dll
¦    Microsoft.Extensions.Configuration.FileExtensions.dll
¦    Microsoft.Extensions.Configuration.Json.dll
¦    Microsoft.Extensions.FileProviders.Abstractions.dll
¦    Microsoft.Extensions.FileProviders.Physical.dll
¦    Microsoft.Extensions.FileSystemGlobbing.dll
¦    Microsoft.Extensions.Primitives.dll
¦     
+---Input
¦    readme.txt
¦    ToolsFirst_Arrows.json
¦    ToolsFirst_Ingredients.json
¦    ToolsFirst_Keys.json
¦    ToolsFirst_Potions.json
¦    ToolsFirst_Scrolls.json
¦    ToolsFirst_SigilStones.json
¦    ToolsFirst_Tomes.json
¦    ToolsFirst_Tools.json
¦       
+---Localization
¦    +---de
¦    ¦    Game.json
¦    ¦       
¦    +---en
¦    ¦    Game.json
¦    ¦       
¦    +---es
¦    ¦    Game.json
¦    ¦       
¦    +---fr
¦    ¦    Game.json
¦    ¦       
¦    +---it
¦    ¦    Game.json
¦    ¦       
¦    +---ja
¦    ¦    Game.json
¦    ¦       
¦    +---pl
¦    ¦    Game.json
¦    ¦       
¦    +---pt
¦    ¦    Game.json
¦    ¦       
¦    +---ru
¦    ¦    Game.json
¦    ¦       
¦    +---zh-Hans
¦         Game.json
¦
+---MagicLoader
     +---GenericModTranslator
          GenericModTranslator_de.zip
          GenericModTranslator_en.zip
          GenericModTranslator_es.zip
          GenericModTranslator_fr.zip
          GenericModTranslator_it.zip
          GenericModTranslator_ja.zip
          GenericModTranslator_pl.zip
          GenericModTranslator_pt.zip
          GenericModTranslator_ru.zip
          GenericModTranslator_zh-Hans.zip
```
# Changelog
## Version 1.0.0
- First stable release
## Version 1.0.1
- Update the MagicLoaderGenerator library to version 1.2.1 to fix problems with the generated Zip archives
## Version 1.1.0
- Updated MagicLoaderGenerator to 1.3.0 and added logging
