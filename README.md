# zfsServices
Some systemd-units for ZFS-enabled hosts.

### Services

#### zfs-autoswap

Creates a zfs volume named `swap`.

On service or manual run this deactivates any active swap devices on the host and removes any swap datasets present on the system before creating a new swap volume on the system with a random passphrase totalling the system's memory in size.

The random and discarded dataset creation passphrase ensures the swap volume's contents won't be recoverable into the next boot (Without modifying the script to store it somewhere).

#### zfs-key-loader

Checks for zfs datasets which are missing their unlock passphrase and prompts for them during the boot process.

### Installation notes and example

The modules can be installed by name with:  `./install zfs-autoswap`

If the repo is not downloaded as a subdirectory under /opt the install script will copy the service script to a subdirectory in /opt unless the repo is already present there.