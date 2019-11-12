# Archlinux-ZFS-Stuff
Little systemd-units, installers and other scripts which lower blood pressure.

zfs-autoswap.service    - Generates a new ZVOL at ${firstPool}/swap of 8G and uses a randomly generated 512char passphrase to do so. Given nobody cares about reading their swap from the last boot.

zfs-key-loader.service  - Checks if there are any unloaded zfs keys and prompts the user for a key to try across all volumes if true.

installServices         - installs and enables those two service files for the next boot.
