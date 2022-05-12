# zfs

> ZFS control commands

- Show info
`zpool status`

- Create stripe
`zpool create {{name}} {{sda1}} {{sda2}}`

- Create mirror
`zpool create {{name}} mirror {{sda1}} {{sda2}}`

- Check errors
`zpool scrub {{name}}`

- Show list available pools
`zpool import`

- Mount pool
`zpool import {{pool}}`

- Unmount pool
`zpool export {{pool}}`
