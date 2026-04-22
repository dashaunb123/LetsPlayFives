# Packaging

Install dependencies once:

```bash
npm install
```

Run the desktop app locally:

```bash
npm start
```

Build a universal macOS app package:

```bash
npm run package:mac:universal
```

Build one Windows NSIS installer containing x64 and ia32 builds:

```bash
npm run package:win:universal
```

Build outputs are written to `dist/`. The artifact names include the `version` from `package.json`, so change that version before packaging a new release.

Notes:
- Package icons are read from `build/icon.png` for macOS and `build/icon.ico` for Windows.
- macOS universal packages require macOS to build cleanly.
- Windows NSIS builds are most reliable on Windows. Cross-building Windows from macOS may require Wine.
- This project has no signing configuration yet, so packaged apps are unsigned.
