# Exhaust
# Exhaust

A small launcher for local Windows games. Point it at a folder, it finds the
`.exe` / `.lnk` files, sorts them, looks up cover art, and gives you a Play button.

Exhaust is a Steam-inspired launcher, not affiliated with or endorsed by Valve or Steam.

## Run

Double-click `exhaust.pyw`. The `.pyw` extension makes Windows use `pythonw.exe`,
so no terminal window opens. (If you had a shortcut to the old `exhaust.py`,
point it at `exhaust.pyw` and delete the old file.)

Needs Python 3.9+ with Tkinter (included with the normal Windows installer).
For cover art, also run: `python -m pip install pillow`

## Using it

- **Set folder** scans a folder and its subfolders. **Rescan** (or F5) refreshes it.
- **Add game** picks a single file, useful for anything outside your folder.
- **Right-click a card** for favorite, rename, category, re-lookup, show in folder, remove.
  Double-click a card to launch it.
- **Tools** has "Fetch game info" and the .rar extraction toggle.
- Installers and redistributables (DirectX, .NET, VC++, crash handlers, uninstallers)
  are skipped automatically.
- With extraction on, `.rar` files in your game folder are unpacked with WinRAR into a
  folder named after the archive, then deleted. If extraction fails, the archive is kept.

## Where things live

`%APPDATA%\Exhaust\` holds `exhaust_data.json` (your library), `covers\`, and
`exhaust.log` (errors go here since there's no terminal).

## Standalone exe (optional)

    pip install pyinstaller
    pyinstaller --onefile --noconsole --name Exhaust exhaust.pyw

## Disclaimer

Exhaust is not meant for pirated games. It's a personal library launcher for
games you own or have the right to use, and it's a Steam-inspired

I'm not liable for how anyone uses it. If you use it for pirated or otherwise
unauthorized software, that's on you, not me.

## License

MIT, with one added condition: if you modify Exhaust and share your version,
you have to say clearly that it's modified and not pass it off as the original.
See the `LICENSE` file for the full text. Copyright (c) 2026 calistabytedotpy OR calistabyte@gmail.com.

