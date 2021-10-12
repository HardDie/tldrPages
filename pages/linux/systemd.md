# systemd

> How to setup systemd boot

- Install
`bootctl install`

- /boot/loader/entries/arch.conf
`title {{Archlinux}}`
`linux /vmlinuz-linux`
`initrd /intel-ucode.img`
`initrd /initramfs-linux.img`
`options root=PARTUUID={{00000000-0000-0000-0000-000000000000}} rw`

- /boot/loader/loader.conf
`default arch`
`timeout {{3}}`
