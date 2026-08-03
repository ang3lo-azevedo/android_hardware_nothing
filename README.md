# Hardware/Nothing for Nothing Phone (1) (Spacewar)

Hardware abstraction layer support for the Nothing Phone (1). Provides the glyph LED control, fingerprint HAL, and Nothing framework integration for AOSP-based ROMs.

## Source History

This fork is based on `DaViDev985/android_hardware_nothing` @ `derp16.2` (forked from `LineageOS/android_hardware_nothing`) with additional patches:

| Source | Branch | Contributions |
|--------|--------|---------------|
| [DaViDev985](https://github.com/DaViDev985/android_hardware_nothing) | [`derp16.2`](https://github.com/DaViDev985/android_hardware_nothing) | Base: NtOnlineConfig stub, ParanoidGlyph, GlyphAdapter, nt-fwk |
| [StudioKeys-Dumps](https://github.com/StudioKeys-Dumps/hardware_nothing) | [`waterlily-qpr2`](https://github.com/StudioKeys-Dumps/hardware_nothing) | NGlyphs/GlyphManager (org.aspends.nglyphs) - 20 commits |
| [kleidione](https://github.com/kleidione/hardware_nothing) | [`bp4a`](https://github.com/kleidione/hardware_nothing) | Fingerprint: Wait for goodix_fp node and add HAL null guards |

## Tree Structure

```
GlyphAdapter/   - Glyph service adapter (used by both ParanoidGlyph and NGlyphs)
NGlyphs/        - GlyphManager app (org.aspends.nglyphs, replaces ParanoidGlyph)
hidl/           - Fingerprint HAL (goodix_fp)
nt-fwk/         - Nothing framework (NtOnlineConfig stub for Nothing Camera)
```

## Features

- **NGlyphs** - System app for glyph LED control, no root required
  - Call and notification LED patterns with audio-glyph sync
  - Recording indicator LED service
  - Music visualizer with stock Nothing behaviour
  - Glyph Converter with Opus-in-Ogg encoding
  - Essential lights, sleep mode, battery animations
  - Third-party app support via GlyphAdapter
- **Fingerprint** - Goodix FP with null guards and node wait fix
- **NtOnlineConfig** - Stub implementation required by Nothing Camera

## Credits

- [DaViDev985](https://github.com/DaViDev985) - hardware/nothing base, NtOnlineConfig stub
- [Jis G Jacob (StudioKeys)](https://github.com/StudioKeys-Dumps) - NGlyphs implementation
- [kleidione](https://github.com/kleidione) - Fingerprint HAL fix
- [LineageOS](https://github.com/LineageOS) - upstream hardware/nothing
