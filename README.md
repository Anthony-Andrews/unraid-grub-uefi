# unraid-grub-uefi
A GRUB bootloader build to enable Unraid UEFI booting on esoteric platforms


## What drove this:
Unraid's stock syslinux bootloader seems to not always play nicely with many older systems, GRUB has much better support for edge-case platforms.
Wanted GPU support on a Dell Poweredge R920, needed UEFI for proper MMIO support for the Nvidia driver to initialize at all.

## Usage:
- on unraid USB root directory, rename the "EFI" folder to "EFI-old" for backup purposes
- download EFI folder to root directory.

## Acknowledegmenets:
- GRUB source [https://gitlab.freedesktop.org/gnu-grub/grub/](https://gitlab.freedesktop.org/gnu-grub/grub/)
- Jank GPU [fitting](https://www.reddit.com/r/homelab/comments/198jn6q/to_those_asking_how_i_powered_the_tesla_p40_and/) (with modified EPS 8-pin off PSU board)

### To Do:
- safe modes
- non-hardcoded drive selection
