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
