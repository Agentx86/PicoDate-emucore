# PicoDate emucore

A PICO-8 cart player core for [CrankBoy](https://github.com/CrankBoyHQ/crankboy-app)
on the Playdate. It is the engine of [PicoDate](https://bitcalibergames.itch.io/picodateplaydate),
the standalone PICO-8 player for Playdate, built as a libcrankemu core.
Based on [fake-08](https://github.com/jtothebell/fake-08) by jtothebell and
[z8lua](https://github.com/samhocevar/z8lua) by Sam Hocevar.

This repository holds the releases and the core descriptor (`ce.json`) for
CrankBoy's core registry ([libcrankemu-cores](https://github.com/CrankBoyHQ/libcrankemu-cores)).
The core's source code is not published.

## Install

1. Download `PicoDate-emucore.zip` from the [latest release](https://github.com/Agentx86/PicoDate-emucore/releases/latest).
2. Connect the Playdate in disk mode and copy `PicoDate.bin` to `/Shared/Emulation/cores/`.
3. Put carts (`.p8.png` or `.p8`) in `/Shared/Emulation/p8/games/`.
4. Start CrankBoy (3.0 or newer, see Requirements): the carts are listed in
   the library next to the other systems.

Multi-cart games: the cart you start goes in `games/`, the carts it loads with
`load()` go in `/Shared/Emulation/p8/carts/` (CrankBoy does not list that
folder). For example Into Ruins: `games/Into Ruins (intoruins-7).p8.png`,
`carts/intoruins_main-7.p8.png` and `carts/intoruins.p8.png`.

Keep the cart's BBS id in its file name (for example
`Breakout Hero (53976).p8.png`): PicoDate's per-cart fixes for the Playdate
find a cart by that id.

## Requirements

- **CrankBoy 3.0 or newer.** Until 3.0 is released, that is CrankBoy built
  from its `development` branch. The core needs what 3.0 gives emulation
  cores (libcrankemu frontend version 2: fast DTCM memory for cores, return
  to the library). In older CrankBoy (2.2.1 and before) the core shows
  "PicoDate needs CrankBoy 3.0 or newer" instead of the game.
- Tested on a Playdate Rev B.

## Controls

- D-pad, A, B: the PICO-8 buttons.
- A + B together: the PICO-8 pause menu.
- Crank: scrolls the picture in the Crop view.

Core settings (in CrankBoy's settings for the game): View (Fit / Crop),
Dither (Rank / Luma), Sound (On / Off). Cartdata is saved like a CrankBoy
save file; save states work through CrankBoy's settings.

## License

Free to download, use and share unmodified (see [LICENSE](LICENSE)). The core
contains open-source components listed in
[THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt), each under its own license.

PicoDate is not affiliated with Lexaloffle Games. PICO-8 is a trademark of
Lexaloffle Games.
