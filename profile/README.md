# Welcome

Here, you'll find plenty of cool things for the amazing game [Valheim](https://www.valheimgame.com/).

Visit the [Valheim Landoria Gaming YouTube channel](https://www.youtube.com/@ValheimLandoriaGaming/videos) for mod demos and Valheim videos.

Browse [Landoria's mods on Thunderstore](https://thunderstore.io/c/valheim/p/Landoria/).

## Mods

First, you'll find mods to customize your Valheim experience. Explore their repositories below:

### Client-only mods

| Mod | Description | Demo | Thunderstore |
| --- | --- | --- | --- |
| [FirstPerson](https://github.com/landoria-gaming/Landoria.FirstPerson) | Adds a smooth first-person view with an adjustable field of view. | [YouTube](https://youtu.be/eExAEyoNsSs) | [Thunderstore](https://thunderstore.io/c/valheim/p/Landoria/FirstPerson/) |
| [FreeFly](https://github.com/landoria-gaming/Landoria.FreeFly) | Adds a free camera for exploring, taking screenshots, and filming without admin permissions. | [YouTube](https://youtu.be/smoOkcAPKr0) | [Thunderstore](https://thunderstore.io/c/valheim/p/Landoria/FreeFly/) |
| [GentleDeath](https://github.com/landoria-gaming/Landoria.GentleDeath) | Keeps equipable items after death and moves other items to your tombstone. | [YouTube](https://youtu.be/O61d6w3ZpVs) | [Thunderstore](https://thunderstore.io/c/valheim/p/Landoria/GentleDeath/) |
| [QuickLaunch](https://github.com/landoria-gaming/Landoria.QuickLaunch) | Automatically resumes your last local world or multiplayer session. | [YouTube](https://youtu.be/K0r75KNOGc0) | [Thunderstore](https://thunderstore.io/c/valheim/p/Landoria/QuickLaunch/) |
| [HuginnCam](https://github.com/landoria-gaming/Landoria.HuginnCam) | **Under development.** Records gameplay from an independent cinematic camera. | — | — |

### Client and server mods

| Mod | Description | Demo | Thunderstore |
| --- | --- | --- | --- |
| [CharacterVault](https://github.com/landoria-gaming/Landoria.CharacterVault) | Stores trusted character saves on the server to prevent item imports and duplication. | [YouTube](https://youtu.be/x2C1DdU_78c) | [Thunderstore](https://thunderstore.io/c/valheim/p/Landoria/CharacterVault/) |
| [HammerFreedom](https://github.com/landoria-gaming/Landoria.HammerFreedom) | Adds server-authorized flight, unlimited stamina, fall protection, and lasting equipment in Hammer worlds. | [YouTube](https://youtu.be/wUBgHzN5hG8) | [Thunderstore](https://thunderstore.io/c/valheim/p/Landoria/HammerFreedom/) |
| [Moderator](https://github.com/landoria-gaming/Landoria.Moderator) | Gives trusted moderators server-authorized tools to help players and manage the world. | [YouTube](https://youtu.be/GxZJFHgpYNY) | [Thunderstore](https://thunderstore.io/c/valheim/p/Landoria/Moderator/) |
| [ModSentry](https://github.com/landoria-gaming/Landoria.ModSentry) | Checks that client mod files and versions match the server's requirements. | — | [Thunderstore](https://thunderstore.io/c/valheim/p/Landoria/ModSentry/) |
| [SealedTombstone](https://github.com/landoria-gaming/Landoria.SealedTombstone) | Protects recent tombstones and lets owners approve access for other players. | [YouTube](https://youtu.be/WzRf7-7_DGg) | [Thunderstore](https://thunderstore.io/c/valheim/p/Landoria/SealedTombstone/) |
| [Socialize](https://github.com/landoria-gaming/Landoria.Socialize) | Adds session groups, private messages, group chat, and shared map positions and pings. | — | [Thunderstore](https://thunderstore.io/c/valheim/p/Landoria/Socialize/) |

## Valheim Docker image

The [Valheim Docker image](https://github.com/landoria-gaming/valheim-server-image/pkgs/container/valheim_server.x86_64) includes the dedicated server and BepInExPack_Valheim. Updates are checked daily, and the image is rebuilt when a new version of Valheim or BepInExPack_Valheim is available.

This means the image normally contains the latest Valheim dedicated server version, once the daily update check and build have completed.

## Harmony Validator

When patching a public method, you can use C#'s `nameof` to let the compiler check its name. Private methods sometimes need to be targeted by a string, which the compiler cannot check.

[Harmony Validator](https://github.com/landoria-gaming/HarmonyValidator) verifies during the build that the targeted method really exists and that the patch parameters match. This makes mods more robust by catching missing methods or incompatible parameter changes at compile time.

Harmony Validator is available on [NuGet](https://www.nuget.org/packages/HarmonyValidator), so you can add it directly to your mod project as a NuGet package. All Landoria mods use this validator.

## More projects

Explore [End3rByte's repositories](https://github.com/end3rbyte?tab=repositories) for more projects beyond Valheim.

## Get in touch

Have a question, an idea, or feedback about these projects? Leave a message in [Landoria's discussions](https://github.com/orgs/landoria-gaming/discussions). You can also share your creations and tell us how you use these projects!

Found a bug? Please open an issue in the affected project's repository and describe what happened and how to reproduce it.
