# [Sega Saturn](https://en.wikipedia.org/wiki/Sega_Saturn) for MiSTer

This implements:

* Sega Saturn home console
* Sega Titan Video (ST-V) arcade board (based on the Saturn)

## Hardware Requirements

- 128 MB SDRAM Module (Primary)
- SDRAM Module of any size (32MB-128MB) (Secondary)

> [!NOTE]
> Dual SDRAM modules is recommended for better compatibility.

## Status

Current status is WIP/Beta

Known issues:

## Build variants

There are two different builds of the core. Single SDRAM and Dual SDRAM.

The Single SDRAM core has known timing problems which can cause slowdown and
other issues in games.

Even the Dual SDRAM core will never be 100% accurate on MiSTer hardware[^9].
This is because the hardware can't provide the access speed necessary to match
the original console[^10].

The Single SDRAM core has a Fast Timings option as a partial mitigation. This
is an option to reduce the accuracy of the core as a workaround for slow RAM
access speed[^12]. (The Dual SDRAM core doesn't have this option because there
is no need for it.)

> [!CAUTION]
> The Fast Timings option can lead to freezes, graphical corruption or other
> issues[^11]. It is recommended to keep this option off, except when playing
> particuar games:
> 
> | Game | Notes |
> | ---- | ----- |
> | Dead or Alive | Enable fast timings to reduce slowdown. |
> | Digital Dance Mix Vol. 1 | Enable fast timings to fix freezes. |
> | Fighters Megamix | Enable fast timings to reduce slowdown. |
> | Fighting Vipers | Enable fast timings to reduce slowdown. |
> | Grandia | Enable fast timings to reduce (but not completely eliminate) texture flicker. |

On the whole Dual SDRAM will perform better.

For example *Digital Dance Mix Vol. 1* will still have slowdown on Single SDRAM
but not on Dual SDRAM. *Pyon Pyon Kyaruru no Mahjong Biyori* will still have
graphical corruption in the intro on Single SDRAM but not on Dual SDRAM.

## Games with bugs on original hardware

There are several games that have bugs on original hardware.
These are not problems with the core.

The following are major bugs that prevent games from starting.

| Game | Bug(s) | Notes |
| ---- | ------ | ----- |
| In the Hunt | 🎮 📅 | Disable 2nd controller, set date in BIOS between 1994 and 1998[^1]. |
| Night Striker S | 🎮 | Disable 2nd controller[^1]. |
| Shinobi Legends/X | 🎮 | Disable 2nd controller[^1]. |

The following are minor issues/glitches.

| Game | Bug(s) | Notes |
| ---- | ------ | ----- |
| Advanced Variable Geo | 👀 👂 | Graphical corruption that can appear under the character portrait on the bottom[^7]. Audio pops and stutters[^6]. |
| Cleopatra Fortune | 👂 | Worse sound mixing compared to the arcade original. |
| Daytona USA | 👀 | HUD obscured by car[^8].
| Goiken Muyou: Anarchy in the Nippon | 👀 | Models flickering on certain stages[^3].
| Madou Monogatari | 👀 | In the prologue, the background from the prior cutscene is still shown as a vertical pink line on the left of the screen. |
| Magical Night Dreams - Cotton 2 | 👀 | Minor visual glitch on the background[^4]. |
| Rabbit | 👀 | Sprite assets are improperly scaled compared to the arcade version. (An [English patch](https://github.com/DerekPascarella/Rabbit-EnglishPatchSaturn) enables option to disable the zoom.) |
| Simulation Zoo | 👀 | Menu overdrawn[^5]. |
| Sonic Wings Special | 👀 | Graphical corruption when chaning screen modes[^2]. |
| Twinkle Star Sprites | 👂 | Heavily compressed audio samples compared to the original Neo Geo version. |

Where the bugs types are defined below.

| Bug | Description |
| --- | ----------- |
| 🎮  | Won't start with a controller in the second controller port. |
| 📅  | System date requirements. |
| 👀  | Visual glitches. |
| 👂  | Audio glitches. |

## References

[^1]: Comment on issue [In The Hunt (Us) not working in 20240206 version and 20240204 version](https://github.com/MiSTer-devel/Saturn_MiSTer/issues/116#issuecomment-1931663872).
[^2]: Comment on issue [Sonic Wings Special [original game bug] - bug when cycling through screen modes](https://github.com/MiSTer-devel/Saturn_MiSTer/issues/293#issuecomment-2511628138).
[^3]: Comment on issue [Goiken Muyou: Anarchy in the Nippon (Japan) // Flickering character models in some stages](https://github.com/MiSTer-devel/Saturn_MiSTer/issues/311#issuecomment-2558405990).
[^4]: Comment on issue [[ORIGINAL GAME BUG] Magical Night Dreams - Cotton 2 (Japan) // Incorrect render of a background on Stage 2 (stripe on left side)](https://github.com/MiSTer-devel/Saturn_MiSTer/issues/365#issuecomment-2671864249).
[^5]: Comment on issue [Simulation Zoo (Japan) // [ORIGINAL GAME BUG] VDP - Possible incorrect masking between a menu & the game date](https://github.com/MiSTer-devel/Saturn_MiSTer/issues/291#issuecomment-2501357691).
[^6]: Comment on issue [Advanced V.G. (Japan) - Audio issues and game crash](https://github.com/MiSTer-devel/Saturn_MiSTer/issues/356#issuecomment-2661555243).
[^7]: Comment on issue [Advanced V.G. (Japan) // Scrambled graphics below opponents animated portraits after a battle stage](https://github.com/MiSTer-devel/Saturn_MiSTer/issues/240#issuecomment-2309006095).
[^8]: Comment on issue [Daytona USA - gui obscured by the car hood](https://github.com/MiSTer-devel/Saturn_MiSTer/issues/228#issuecomment-2272840947).
[^9]: Comment on issue [Fighters Megamix // Skipping Intro Cutscene Freezes Game](https://github.com/MiSTer-devel/Saturn_MiSTer/issues/136#issuecomment-2449438355).
[^10]: Comment on issue [Fighters Megamix // Skipping Intro Cutscene Freezes Game](https://github.com/MiSTer-devel/Saturn_MiSTer/issues/136#issuecomment-2449280850).
[^11]: Comment on issue [Pyon Pyon Kyaruru no Mahjong Biyori // Corruption In Intro On Single RAM Build (10-30-2024~)](https://github.com/MiSTer-devel/Saturn_MiSTer/issues/251#issuecomment-2481418725).
[^12]: Comment on issue [Pyon Pyon Kyaruru no Mahjong Biyori // Corruption In Intro On Single RAM Build (10-30-2024~)](https://github.com/MiSTer-devel/Saturn_MiSTer/issues/251#issuecomment-2482401756).
