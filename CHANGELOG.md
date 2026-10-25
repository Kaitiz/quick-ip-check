# Changelog

## 2.1.4 — 2026-10-25

- UI improvements.

## 2.1.3 — 2026-10-24

- Bug fixes.

## 2.1.2 — 2026-10-22

- Uses less memory: the main window and Settings are released when closed instead of updating in the background.
- Menu bar text updates once per check instead of once per changed value.
- While the Internet is down, re-checks every 2 seconds for the first half minute, then less often during a long outage.

## 2.1.1 — 2026-10-21

- Shows the IP type: residential, business, mobile, data center, VPN or Tor (combined from ip-api.com, fFraud and proxycheck.io; Settings → Reputation).
- Option to show the IP's location (city and country code, or country name) instead of the ISP name in the menu bar (Settings → Display, off by default).
- Local IPs name Tailscale as "Tailscale"; "VPN" is used only for a VPN that carries Internet traffic, other tunnels show as "Tunnel". The status label only says VPN when Internet actually goes through one.
- Fixed the history table's column titles not lining up with the rows in the main window.

## 2.1 — 2026-10-21

- Main window: open Quick IP Check like a regular app ("Open Window" in the menu bar panel, or the right-click menu), with the overview, today's stats, a 7-day chart of IP changes, and a searchable, filterable history table side by side. While it's open the app appears in the Dock.
- Shorter menu bar: show the IP in full, as "203…45", "113.45" or just "45", and the ISP by name or initials. Settings → Display.
- Pauses checking while the Mac sleeps or the screen is locked, and checks right away when you're back (Settings → General, on by default).
- Redesigned Settings with a sidebar, clearer grouping (new VPN page) and a live menu bar preview.
- The status label names the connection, e.g. "Wi-Fi · Connected" or "Ethernet · Connected".

## 1.5 — 2026-10-21

- History marks IPs that came through a VPN with a "VPN" tag, also exported as a VPN column in CSV.
- Identifies the VPN in use: its name (e.g. NordVPN, ProtonVPN) and Tailscale exit nodes, with the exit node's name. Both can be turned off in Settings → Display.

## 1.4 — 2026-10-21

- With a VPN, the menu bar now shows only the current public (VPN) IP. Choose "ISP IP → VPN IP" in Settings → Display to show both.
- Fixed typing a check interval (e.g. "10" turned into "50").
- Fixed the ISP IP shrinking and growing in the overview while a VPN is on.
- Fixed the "VPN blocks all traffic outside the tunnel" note appearing and disappearing while a VPN is on.

## 1.3 — 2026-10-21

- Three more IP reputation services that need no API key: fFraud, ip-api.com and StopForumSpam (Settings → Reputation). proxycheck.io remains the default.

## 1.2.1 — 2026-10-21

- Fixed VPNs that send all traffic through the tunnel being reported as "split tunnel". When such a VPN hides the ISP IP, the last ISP IP seen before the VPN is shown instead.

## 1.2 — 2026-10-21

- Set a maximum number of history entries (50, 100, 200, 500, 1,000 or unlimited) in Settings → History, alongside auto-delete. Oldest entries are removed first.

## 1.1 — 2026-10-21

First public release.

- Public IP and short ISP name in the menu bar (`VNPT · 203.0.113.45`), with short names for providers worldwide.
- VPN aware: shows both the VPN IP and the original ISP IP.
- Re-checks right away when the network drops and comes back or the Mac wakes; otherwise every 3 minutes (adjustable).
- IP history recorded only when the IP changes, with automatic cleanup (6 hours to 1 month) and CSV export.
- Popup when the IP changes (1–5 s, top left / center / right), noting when a returning IP was last used.
- IP reputation score from proxycheck.io, AbuseIPDB or IPQualityScore.
- Local IPv4 / IPv6 per network interface.
- One-click updates: downloads, verifies (SHA-256), installs and reopens.
- English and Vietnamese, light and dark mode, open at login.
