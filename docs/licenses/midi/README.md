# Shared MIDI sound bank

- `timgm6mb.sf2`: unmodified full TimGM6mb 1.3 sound bank (5,969,788 bytes). This is the sound bank currently imported by the frontend.
- `timgm6mb-llk.sf2`: subset for the 17 original Lianliankan MIDIs (3,404,198 bytes, 60 presets). Retained for comparison; not currently used by the frontend.
- `TimGM6mb.copyright` and `LICENSE-GPL-2.0.txt`: attribution and license for both versions.

Source: https://deb.debian.org/debian/pool/main/t/timgm6mb-soundfont/timgm6mb-soundfont_1.3.orig.tar.gz

The subset removes unused presets and sample zones, without resampling or lossy compression. Rebuild it when adding or changing the Lianliankan MIDI files:

```sh
node packages/game-assets/scripts/trim_llk_soundbank.mjs
```
