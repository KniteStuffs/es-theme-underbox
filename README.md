# es-theme-underbox

An **Undertale-inspired dark theme** for EmulationStation on **ArkOS**, designed for the **R36S** handheld (640×480).

It keeps the layout of the *NES Box* theme and re-skins it: black screens, pixel borders, pixel-font logos, character art for selected systems, and a color option you can change from the menu.

> **BETA NOTICE:** This theme is still a work in progress. Only 10 systems currently have custom character art. The remaining systems will display a pixelated heart in a variety of colors until their character art is added. You can add the missing character art yourself if you don't want to wait for future updates.

> Unofficial fan project. Not affiliated with or endorsed by Toby Fox, Nintendo, Sony, Sega, or anyone else mentioned.


## Features

- **Colorset option** – Change the color of the frames, bottom bar, system logos, and highlighted game from *Start → UI Settings → Theme Configuration → Colorset*. Choices: White (default), Yellow, Orange, Red, Green, Cyan, Blue, and Purple.
- **Per-system logos** – Pixel-style text logos for 80+ systems, including NES, SNES, GB/GBC/GBA, N64, DS, Mega Drive/Genesis, PSX, PSP, Dreamcast, arcade, and more. Systems without a custom logo fall back to their name as text.
- **Character art (BETA)** – Currently, only the following 10 systems have custom character art:
  - PICO-8
  - RetroArch
  - N64
  - NDS
  - Kodi
  - PSP
  - Ports
  - All Games
  - Favorites
  - Movies

  Character art for all other systems is still a work in progress. These systems will display a pixelated heart in a variety of colors until their character art is added.

  If you don't want to wait for future updates, you can add the missing character art yourself by following the instructions in the **Customizing** section.
- **Dark Start menu** – Black window, white text, and colored selection. Requires an ArkOS build that supports menu theming.
- **Navigation sound** – A short sound when scrolling through the game list or systems.
- **Multiple game list views** – Detailed, basic, and video views, with support for box art, ratings, release dates, developers, publishers, and descriptions.
- **Optimized for the R36S** – Positions use normalized (0–1) coordinates, and text sizes are chosen for the 3.5-inch, 640×480 screen.

## Installation

1. Download this repository and make sure the folder is named **`es-theme-underbox`**.
2. Copy the folder to one of these locations on your R36S:
   - SD card `EASYROMS` partition: `themes/es-theme-underbox/` (appears as `/roms/themes/`).
   - Or `/etc/emulationstation/themes/es-theme-underbox/`.
3. On the device, go to **Start → UI Settings → Theme Set → es-theme-underbox**.
4. To change the color, go to **Start → UI Settings → Theme Configuration → Colorset**.

   If the colors don't change, restart EmulationStation.

## Customizing

- **Add or change a system logo:** Put a 384×192 transparent PNG named `logo.png` in that system's folder.
- **Add or change a character:** Replace `art.png` (large, displayed on the system screen, maximum approximately 320×360) and `art_small.png` (small, displayed on game lists, maximum approximately 70×72) in that system's folder.
- **Add missing character art:** Find the folder for the system you want to customize and add your own `art.png` and `art_small.png` files. This lets you replace the default colored pixelated heart with your own character artwork.
- **Missing system?** Copy an existing system folder, rename it to match your system's theme name (see `es_systems.cfg`), and replace the images.
- **Blurry text?** Try setting `fontSize` to `0.0333` or `0.05` in `theme.xml`.

## Folder Layout

```text
es-theme-underbox/
├── theme.xml            # Main theme: system view, game lists, and menu
├── _inc/
│   ├── colors/          # Colorset files (white, yellow, etc.)
│   ├── fonts/           # Determination Mono font
│   ├── images/          # Backgrounds and overlays
│   └── sounds/          # Navigation sound (WAV)
└── <system>/            # One folder per system
    ├── theme.xml
    ├── logo.png
    ├── art.png
    └── art_small.png
```

## Compatibility

Made for **ArkOS and EmulationStation on the R36S, Tested on dArkOSen**.

The Colorset and menu theming options depend on the features supported by your particular ArkOS build. If an option doesn't work, open an issue and include your ArkOS version.

As this theme is currently in beta, some systems may have incomplete artwork or features. Updates will add more character art and improvements over time.

## Credits

- **NES Box Theme (v2.0)** – Original layout by Travis Wilson / Super Retro City.
- **Undertale** – Created by Toby Fox. Character art, sound effects, and referenced fonts belong to their respective creators. See `CREDITS.md` for the list of artwork credits.
- **System names** – Used only as text labels. No official console logos are included.

## License

Add a license of your choice for your own work (for example, MIT for the XML and original generated images).

Third-party material, including the original NES Box layout, Undertale assets, fonts, and character art, remains subject to its respective owners' terms.

