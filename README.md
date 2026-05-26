# unraid-grub-uefi
A modified GRUB build to enable Unraid UEFI booting on esoteric platforms


## What drove this:
I was attempting to get GPU support under Unraid on a Dell PowerEdge R920 quad-socket server, after much pain I found Dell's half broken UEFI implementation was the only way to get proper MMIO for the Nvidia driver to initilize without error.
Unraid's stock syslinux bootloader was unable to boot at all under UEFI which drove me to hodge together a GRUB-based bootloader for Unraid installs.

## Usage:
- on unraid USB root directory, rename the "EFI" folder to "EFI-old" for backup purposes
- download EFI folder to root directory.

## Acknowledgmenets:
- GRUB source [https://gitlab.freedesktop.org/gnu-grub/grub/](https://gitlab.freedesktop.org/gnu-grub/grub/)
- Jank GPU [fitting](https://www.reddit.com/r/homelab/comments/198jn6q/to_those_asking_how_i_powered_the_tesla_p40_and/) (with modified EPS 8-pin off PSU board)
