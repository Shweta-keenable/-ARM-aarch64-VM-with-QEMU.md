## How to launch ARM aarch64 VM with QEMU from scratch. 

To launch a To launch an arch64 VM we first need to install a few dependencies, including QEMU and the qemu-efi-aarch64 package, 
which includes the efi firmware.

apt-get install qemu-system-arm

apt-get install qemu-efi-aarch64

apt-get install qemu-utils

## Create the flash images with the correct sizes.

dd if=/dev/zero of=flash1.img bs=1M count=64

dd if=/dev/zero of=flash0.img bs=1M count=64

dd if=/usr/share/qemu-efi-aarch64/QEMU_EFI.fd of=flash0.img conv=notrunc


Download the image you want to boot.

For our example we use an Ubuntu installer.
