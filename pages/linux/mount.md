# mount

> Usefull mount commands

- Remount disk to rw mode
`mount -o remount,rw {{/mounted/path}}`

- How to mount with permissions
`mount -o umask=000 {{/dev/sda}} {{/mnt}}`
