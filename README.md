# Kid Chameleon — Music Fix (NTSC)

An IPS patch that smooths out the music timing in the original Sega Genesis game.

## What it fixes

Kid Chameleon's GEMS sound driver advances the music on the video frame clock. Musical intervals don't always divide evenly into frames, so otherwise steady rhythms can alternate between slightly shorter and longer gaps.

This patch moves the music clock to the YM2612's Timer B. It alternates between adjacent timer periods to keep the intended tempo with much finer timing. Timer A continues to handle sampled audio. Original notes, instruments, intros, loop points, and gameplay are preserved.

## Compatibility

- Designed for **NTSC Genesis / Mega Drive** timing.
- Boot-tested in **Kega Fusion 3.64**. Driver tests cover 13 music sequences and 13 representative sound effects.
- Physical hardware testing and a full game playthrough are still needed. PAL timing and other ROM revisions have not been verified.

## Credits

- **Sega / Sega Technical Institute** — original game.
- **[Sonic Retro and contributors](https://github.com/sonicretro/kid-chameleon-disasm)** — disassembly.
- **[Valley Bell](https://github.com/ValleyBell/GEMSPlay)** — GEMS source references used during development.
- **ChatGPT-6.1 Sol was utilized in the creation of this patch.
