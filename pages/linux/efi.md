# efi

> How to create single boot efi file

- Bash script
`#!/bin/bash`
`INITRAMFS="/boot/intel-ucode.img /boot/initramfs-linux.img"`
`CMDLINE="root=UUID=00000000-0000-0000-0000-000000000000 rw quite loglevel=3"`
`cat ${INITRAMFS} > initramfs.img`
`objcopy \`
`        --add-section .osrel=/etc/os-release --change-section-vma .osrel=0x20000 \`
`        --add-section .cmdline=<(echo ${CMDLINE}) --change-section-vma .cmdline=0x30000 \`
`        --add-section .linux=/boot/vmlinuz-linux --change-section-vma .linux=0x2000000 \`
`        --add-section .initrd=initramfs.img --change-section-vma .initrd=0x3000000 \`
`        /usr/lib/systemd/boot/efi/linuxx64.efi.stub arch.efi`
`rm initramfs.img`
