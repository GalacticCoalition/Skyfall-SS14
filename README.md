<p align="center"> 
  <img alt="Space Station 14" width="880" height="300" src="https://raw.githubusercontent.com/space-wizards/asset-dump/de329a7898bb716b9d5ba9a0cd07f38e61f1ed05/github-logo.svg" />
</p>

Welcome to the Skyfall community server for Space Station 14, a remake of SS13. This game runs on the [Robust Toolbox](https://github.com/space-wizards/RobustToolbox), a custom engine developed by the Space Wizards team and written in C#.

## About this Repository

This is a repository specifically tailored for the Skyfall server. It's important to note that while we host and create content for SS14, **we are not the original creators of the Robust Toolbox or the main SS14 content**. These tools were developed by the Space Wizards team.

Our repository contains both RobustToolbox and the unique content pack developed for Skyfall, making it an essential tool for those interested in developing additional content for our server.

## Links

[Website](https://spacestation14.io/) | [Discord](https://discord.ss14.io/) | [Forum](https://forum.spacestation14.io/) | [Steam](https://store.steampowered.com/app/1255460/Space_Station_14/) | [Standalone Download](https://spacestation14.io/about/nightlies/)

## Documentation/Wiki

Our [docs site](https://docs.spacestation14.io/) has extensive documentation on SS14's content, engine, and game design, in addition to numerous resources for those interested in contributing to the project.

## Contributing

**__MODULARISATION GUIDELINES:__**

**IMPORTANT:** We operate on a strict zero-tolerance non-modularity directive, meaning that all additional content MUST be fully modular and follow this guide. It is absolutely possible to make most if not all additions modular. If you need to change something within the central content pack then this must be taken upstream.

**Failure to follow this simple directive will result in your content being denied. No exceptions.**

How you make your additional content will depend on what practical changes will be required. There are two categories for modularisation: Assembly-Type and Resource-Type.

Assembly-Type:
Assembly type changes are changes that require modification to the C# assembly, such as a code related change. To achieve this you must add your new C# code to the relevant Skyfall assembly. An example of this would be: Adding a new CI system. You'd first assess what changes need to be made and what parts of the game need changed(client, server, etc.) and then navigate to the relevant assembly(e.g. Content.Client) and make your additions in the Skyfall folder(Content.Client/Skyfall).

Resource-Type:
Resource type changes are changes that do not require modification to how the game runs(think prototypes, textures, audio etc), and thus requires no C# changes. This means you are able to simply create the new file containg your additional content without interfering with any existing resources. An example of this would be: Adding a new food type. This requires no code changes and all you need to do is create a new YML file in the relevant directory within the Skyfall modular folder (Resources/Prototypes/Skyfall/Hydroponics/Seeds.yml). This primarily relates to new prototypes.

Hybrid-Type:
These incorporate both of the above and may be required in some scenarios. It is entirely fine for you to utilise both.

## Building

1. Clone this repo.
2. Run `RUN_THIS.py` to init submodules and download the engine.
3. Compile the solution.

For [more detailed instructions on building the project](https://docs.spacestation14.io/getting-started/dev-setup).

## License

All code for the content repository is licensed under [MIT](https://github.com/space-wizards/space-station-14/blob/master/LICENSE.TXT).

Most assets are licensed under [CC-BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) unless stated otherwise. Please note that some assets are licensed under the non-commercial [CC-BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/) or similar non-commercial licenses and will need to be removed if you wish to use this project commercially.
