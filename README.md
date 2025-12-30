# chitubox-flatpak
Flatpak builder for Chitubox

# Why
Chitubox does not provide a flatpak, and their tarball requires some specific libraries that can be a pain on modern
systems.  This flatpak keeps you from having to install older libraries and sandboxes the software as well.

Additionally, because this is proprietary software it will likely never be in Flathub, so you have to build it yourself.

# Building and Installing
1. [Download Chitubox](https://www.chitubox.com/en/download/previous/chitubox-free) tarball to the repo directory
    * Note: As of 2025-12-30 1.9.5 is the last version that works with Linux.
1. Make sure you have user-level flathub access: `flatpak remote-add --user --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo`
1. Run `flatpak-builder --force-clean --user --install-deps-from=flathub --install build/ com.chitubox.Chitubox.yml`
1. Find "Chitubox" in your desktop menus or run `flatpak run com.chitubox.Chitubox`
