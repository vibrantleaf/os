## Changes from upstream.
Hello, here is a list of the changes that I have made in this soft-fork so far.

- Added: [Microsoft](https://github.com/microsoft/)/[mimalloc](https://github.com/microsoft/mimalloc/)
  - Added: `ujust` script to enable and disable mimalloc globally via `LD_PRELOAD` in `/etc/environment`
- Added: [root0emir](https://github.com/root0emir)/[ArchLinux-GamingPerformanceTuning's](https://github.com/root0emir/ArchLinux-GamingPerformanceTuning/) [sysctl.conf](https://github.com/root0emir/ArchLinux-GamingPerformanceTuning/blob/main/Settings/sysctl.conf)
- Added: [Feral Interactive](https://github.com/FeralInteractive/)/[gamemode](https://github.com/FeralInteractive/gamemode)
- Enabled: NTSYNC Kernel Module by default

## how to rebase
Run `fastfetch` in the Terminal to get your image-name, it should at be arround the top of the output and will probably  be something like `bazzite`, `bazzite-deck`, `bazzite-gnome` or `bazzite-gnome-deck` or alike.
Then Run the following in the Terminal to rebase, you will need to restart your device after rebasing.
```bash
pkexec bootc switch ghcr.io/vibrantleaf/image-name:stable
```
> It is Highly Recommend that you verify the image's using cosign before rebasing.
```bash
curl -Lo cosign.pub https://raw.githubusercontent.com/vibrantleaf/bazzite/refs/heads/leaf/cosign.pub
cosign verify --key cosign.pub ghcr.io/vibrantleaf/image-name:stable
rm cosign.pub
```