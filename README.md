<p align="center"><img src="docs/icon.png" width="128" alt="LaunchWarden icon"></p>

# LaunchWarden

See and control **everything** that starts with your Mac — not just what *System Settings › General › Login Items & Extensions* chooses to show you.

- **One list for every source**: user and global LaunchAgents, LaunchDaemons, agents/daemons/login items embedded in apps, and the Background Task Management (BTM) database that System Settings reads.
- **Real state**: running (with PID), loaded, disabled or orphaned, read live from `launchd`.
- **Real target**: the actual executable or script behind each item (even `/bin/sh some-script.sh`), its parent app, its plist.
- **Signature check**: Apple, Developer ID (with Team ID) or unsigned.
- **Actions**: show in Finder, copy path, enable/disable, and remove — removal never deletes anything, the plist is moved to a quarantine folder so you can undo.
- Icons and names like System Settings, English and French interface (follows your system language).

## Download

**[⬇︎ Download LaunchWarden 0.1 (DMG)](https://github.com/blckdvc/LauchWarden/raw/main/dist/LaunchWarden-0.1.dmg)** — open it and drag LaunchWarden into Applications.

SHA-256: `e609368c1578b3f444e725e3780e9575c31d7b5f4198112010dda08c1d37623c`

**Requires macOS 26 (Tahoe) on Apple silicon.**

### First launch

The app is not notarized (no paid Apple developer account), so macOS blocks it once:

1. Double-click LaunchWarden (it will be blocked).
2. Go to **System Settings › Privacy & Security**, scroll down and click **Open Anyway**.

If macOS says the app is "damaged", run this once in Terminal:

```
xattr -dr com.apple.quarantine /Applications/LaunchWarden.app
```

To see the full BTM database (what System Settings groups by developer), click the lock button and enter your administrator password.

## Support

by **blckdvc** — free to use. If you feel like it, buy me a few tokens:

[![Buy me tokens](docs/buy-me-tokens.png)](https://paypal.me/lbenh)
