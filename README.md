# TIF2 Enhanced

A native PC version of **This Is Football 2** (PlayStation, 2000, PAL
`SCES-03070`), made by static recompilation, with optional enhancements:
widescreen, a wider match camera, goalkeeper shirt numbers, a full radar,
sharp high-resolution rendering and more.

**You need your own copy of the game.** TIF2psx contains no game disc, game
data or Sony BIOS. It reads everything from a disc image you make from your
own PAL disc.

> Non-commercial fan project. Not affiliated with or endorsed by Sony
> Interactive Entertainment. "This Is Football" is a trademark of its owner.

---
<img width="2547" height="1349" alt="launcher" src="https://github.com/user-attachments/assets/104342f0-ea24-4d24-ac00-2c1c1b18f46f" />

<img width="2560" height="1440" alt="gameplay" src="https://github.com/user-attachments/assets/7d10ee1d-804b-46c4-b37f-52ed3e3f7eb9" />

<img width="2560" height="1440" alt="teamnames" src="https://github.com/user-attachments/assets/1de8439b-a3c9-44c1-87a3-c52a9c687f7b" />

## Requirements

- Windows 10 or 11, 64-bit
- A graphics card with OpenGL 3.3 support (practically any GPU from the last ten years)
- A disc image of **This Is Football 2, PAL, SCES-03070** in BIN/CUE format,
  made from your own disc (see below). Other versions are not supported.
- A gamepad is recommended (Xbox, PlayStation and most other controllers
  work); keyboard works too.

## Installation

1. Download `TIF2psx-v<version>-windows-x64.zip` from the
   [Releases](../../releases) page.
2. Unzip it to a folder of your choice, for example `C:\Games\TIF2psx`.
   Do not run it from inside the ZIP.
3. Put your disc image (`.cue` and `.bin`) into that folder or into a
   subfolder of it.
4. Start `TIF2psx.exe`. The launcher finds the disc image by itself; if it
   does not, choose the `.cue` file in the launcher.
5. Press **PLAY**.

Windows may show "Windows protected your PC" on the first start because the
program is not signed. Click **More info → Run anyway**.

Everything stays in this folder: settings, memory cards (`saves`) and the
data built from your disc (`cache`). To uninstall, delete the folder.

## Making the disc image

Use your own original disc and a CD drive.

- **Windows, simple:** [ImgBurn](https://www.imgburn.com/) → *Create image
  file from disc* → output **BIN/CUE**.
- **Most accurate:** [Redump](http://wiki.redump.org/index.php?title=Dumping_Guides)
  dumping guides (for example with DiscImageCreator or MPF).

TIF2psx checks the image. A wrong or modified image is reported in the
launcher.

## Enhancements

Everything can be switched on or off in the launcher (**General** page for the
main options, **Advanced** for all settings). The **Recommended** preset turns
on the first group; **Classic HD** keeps the original game and only renders
it sharper.

| Enhancement | What it does | Default |
|---|---|---|
| Widescreen 16:9 | Matches in 16:9 through the game's own WIDE SCREEN option; menus stay 4:3 | On |
| Side Camera Distance | Match camera further back for a wider view of the pitch | On |
| Goalkeeper Numbers | Goalkeepers wear their shirt number like every other player | On |
| Radar: All Players | The radar always shows all 22 players | On |
| Visual Preset | Modern (smooth textures, no dither grain) or PS1 Native | Modern |
| PGXP Precision | Steady players and pitch, no wobbling or warping textures | On |
| Internal Resolution | Renders at your monitor's resolution (or higher) | Auto |
| Edited Data: Club Names | Real club names (as of 2000), built from your own disc | Off |
| Frame Rate | Blends the game's 25 pictures per second for smoother motion (light ghosting) | Off |

## Controls

Controllers are set up under **Advanced → Controllers & memory cards** in the
launcher. Memory card 1 is on by default and saved in `saves\card1.mcd`.

## Tips and troubleshooting

- **Uneven motion / stutter:** the game runs in exclusive fullscreen. On a
  G-Sync or FreeSync monitor, make sure variable refresh is enabled for
  fullscreen in the graphics driver. Close other heavy programs while playing.
- **The launcher does not find the disc:** the `.cue` and `.bin` must be next
  to each other and the `.cue` must name the `.bin` correctly. Choose the
  `.cue` by hand in the launcher.
- **Antivirus warning:** unsigned new programs are sometimes flagged. The
  SHA-256 checksum of every release is published next to the download.
- **Reset everything:** delete `settings.toml` and the `mods\state.toml` file
  in the TIF2psx folder (memory cards in `saves` are kept).

## Credits and licenses

- Recompilation framework: [PSXRecomp](https://github.com/mstan/psxrecomp)
  by Matthew Stanley, PolyForm Noncommercial License 1.0.0.
- Launcher: recomp-ui by Matthew Stanley, MIT License.
- BIOS: [OpenBIOS](https://github.com/grumpycoders/pcsx-redux) from the
  PCSX-Redux project, MIT License.
- Further libraries and their licenses: see the `licenses` folder.

Because of the PolyForm Noncommercial license, TIF2psx may not be sold or used
commercially.

**This Is Football 2** © Sony Computer Entertainment. All rights to the game
remain with their owners; TIF2psx only runs a copy you own.
