# Privacy Policy

Effective date: November 21, 2026

Glintcast is an independent Chromium extension for Twitch (`https://www.twitch.tv`). It is not affiliated with or endorsed by Twitch.

## Data Glintcast Stores

All data stays strictly inside your local browser profile (`chrome.storage.local` and Twitch-origin `localStorage`). Glintcast operates no backend servers, collects no analytics, and sends zero telemetry.

| Stored item | Storage location | Purpose |
|---|---|---|
| Preferences (layout, theme, chat, sidebar, player toggles) | `chrome.storage.local` (`settings`) | Sync your settings across open Twitch tabs |
| Verified partner logins (up to 1,000 usernames) | `chrome.storage.local` (`partners`) | Show Twitch Partner seals on sidebar cards |
| Saved Twitch accounts (optional, user-initiated) | `chrome.storage.local` (`accounts`) | Swap saved `twitch.tv` session cookies when you use Switch Account |
| Last chosen volume, upscaling mode, audio compressor state, and boot flags | `localStorage` on `www.twitch.tv` | Restore player preferences immediately at page start |

## Permissions Used

| Permission | Scope | Why Glintcast requests it |
|---|---|---|
| `storage` | Local browser profile | Save preferences, partner seals, and optional saved accounts locally |
| `cookies` | `https://*.twitch.tv/*` | Read and swap `twitch.tv` auth cookies only when you save, switch, or remove an account in the profile menu |
| `scripting` | `https://www.twitch.tv/*` | Apply content-script updates in place without refreshing your active stream |
| Host access | `https://*.twitch.tv/*` | Style Twitch, read React component state for sidebar/chat/player tools, and swap account cookies |

*(Unpacked developer builds also declare `alarms` locally for automatic reload on disk changes; packaged Store and Direct release builds strip `alarms` and all developer reload scripts.)*

## Network Activity

- Glintcast makes no requests to any Glintcast or third-party analytics server.
- Sidebar category icons perform `HEAD` / image requests directly to Twitch’s own static CDN (`static-cdn.jtvnw.net`) to resolve category box art.
- In the **Direct** edition, optional stream ad mitigation relays Twitch’s own playback manifest requests directly to Twitch’s servers (`gql.twitch.tv` / Twitch HLS edges) from your browser.

## Deleting Your Data

- Remove any saved Twitch account individually from the profile menu (**Switch Account → Remove**).
- Reset settings from **All settings → Reset**, or uninstall Glintcast from your browser’s Extensions page to erase all local extension storage immediately.

## Contact

Report privacy or security issues at https://github.com/descentiles/glintcast/issues.

Copyright © 2026 Glintcast. All rights reserved.
