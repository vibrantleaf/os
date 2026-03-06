## Changes from upstream.
Hello, Here is the changes that I have made in this os image derived from bazzite with gnome.
- Added: [Microsoft](https://github.com/microsoft/)/[mimalloc](https://github.com/microsoft/mimalloc/)
  - Added: `ujust` script to enable and disable mimalloc globally via `LD_PRELOAD` in `/etc/environment`
- Added: [root0emir](https://github.com/root0emir)/[ArchLinux-GamingPerformanceTuning's](https://github.com/root0emir/ArchLinux-GamingPerformanceTuning/) [sysctl.conf](https://github.com/root0emir/ArchLinux-GamingPerformanceTuning/blob/main/Settings/sysctl.conf)
- Added: [Feral Interactive](https://github.com/FeralInteractive/)/[gamemode](https://github.com/FeralInteractive/gamemode)
- Added: [vibrantleaf](https://gitlab.com/vibrantleaf/)/[systemd-curfew](https://gitlab.com/vibrantleaf/systemd-curfew)
- Enabled: NTSYNC Kernel Module by default

## How to Rebase.
### Basic
```bash
cosign verify --key https://raw.githubusercontent.com/vibrantleaf/bazzite/refs/heads/leaf/cosign.pub ghcr.io/vibrantleaf/os:stable
pkexec bootc switch ghcr.io/vibrantleaf/os:stable
```
### Deck
```bash
cosign verify --key https://raw.githubusercontent.com/vibrantleaf/bazzite/refs/heads/leaf/cosign.pub ghcr.io/vibrantleaf/os-deck:stable
pkexec bootc switch ghcr.io/vibrantleaf/os-deck:stable
```
### NVidia
```bash
cosign verify --key https://raw.githubusercontent.com/vibrantleaf/bazzite/refs/heads/leaf/cosign.pub ghcr.io/vibrantleaf/os-nvidia:stable
pkexec bootc switch ghcr.io/vibrantleaf/os-nvidia:stable
```