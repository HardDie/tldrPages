# efi

> efi

- How to create single boot efi file
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

- Generate PK - with password for sign binary files
`openssl req -new -x509 -newkey rsa:2048 -sha256 -days 365 -subj "/CN=Platform Key" -keyout {{PK.key}} -out {{PK.pem}}`

- Generate KEK
`openssl req -new -x509 -newkey rsa:2048 -sha256 -days 365 -subj "/CN=Key Exchange Key" -keyout {{KEK.key}} -out {{KEK.pem}}`

- Generate ISK
`openssl req -new -x509 -newkey rsa:2048 -sha256 -days 365 -subj "/CN=Image Signing Key" -keyout {{ISK.key}} -out {{ISK.pem}}`

- Convert to UEFI format
`cert-to-efi-sig-list -g "$(uuidgen)" {{PK.pem}} {{PK.esl}}`
`cert-to-efi-sig-list -g "$(uuidgen)" {{KEK.pem}} {{KEK.esl}}`
`cert-to-efi-sig-list -g "$(uuidgen)" {{ISK.pem}} {{ISK.esl}}`

- Create db.esl
`cat {{ISK.esl}} > {{db.esl}}`

- PK sign by PK
`sign-efi-sig-list -k {{PK.key}} -c {{PK.pem}} PK {{PK.esl}} {{PK.auth}}`

- KEK sign by PK
`sign-efi-sig-list -k {{PK.key}} -c {{PK.pem}} KEK {{KEK.esl}} {{KEK.auth}}`

- db sign by KEK
`sign-efi-sig-list -k {{KEK.key}} -c {{KEK.pem}} db {{db.esl}} {{db.auth}}`
`Write *.auth files to UEFI in order db, KEK, PK`

- Sign binary
`sbsign --key {{ISK.key}} --cert {{ISK.pem}} --output {{bootx64.efi}} {{some_image.EFI}}`
