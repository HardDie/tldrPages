# windows

> Windows usefull info

- Create install flash. Select DOS type and set partition type 07 HPFS/NTFS/exFAT
`mkfs.ntfs -f {{/dev/sda1}}`
`mount {{/dev/sda1}} {{/mnt/flash}}`
`mount -o loop {{win.iso}} {{/mnt/iso}}`
`cp -av {{/mnt/iso}}/* {{/mnt/flash}}`
`umount {{/mnt/flash}}`
`ms-sys -n {{/dev/sda1}}`
`ms-sys -7 {{/dev/sda}}`
