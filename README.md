# Hardware: Nothing Phone (1)

NGlyphs LED HAL and related hardware support for Nothing Phone (1) on VoltageOS.

## NGlyphs

System app replacement for Nothing's Glyph LED interface. No root required.

Features:
- LED notification patterns
- Audio-glyph synchronization
- Music visualizer
- Recording LED indicator

Based on 20 commits cherry-picked from [StudioKeys-Dumps](https://github.com/StudioKeys-Dumps/hardware_nothing) `waterlily-qpr2` branch.

## Components

- NGlyphs LED HAL service
- Fingerprint HAL
- Nothing-specific hardware abstraction

## Branches

| Branch | Android | User |
|--------|---------|------|
| `lineage-24.0` | 17 | VoltageOS |
| `16.2-nglyphs` | 16 | VoltageOS (legacy) |
| `16.2` | 16 | DaViDev985 base |
| `16.0` | 16 | Archive |

## Credits

- [DaViDev985](https://github.com/DaViDev985/android_hardware_nothing) — ParanoidGlyph base
- [StudioKeys-Dumps](https://github.com/StudioKeys-Dumps/hardware_nothing) — NGlyphs implementation
- [LineageOS](https://github.com/LineageOS) — hardware/nothing base

## Maintainer

Ângelo Azevedo
