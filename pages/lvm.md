# lvm

> How to setup lvm

- Create physical volume
`pvcreate {{/dev/sda1}} {{/dev/sda2}}`

- Show physical volumes
`pvdisplay`

- Create volume group
`vgcreate {{groupName}} {{/dev/sda1}} {{/dev/sda2}}`

- Show volume groups
`vgdisplay`

- Deactivate volume group
`vgchange -a n {{groupName}}`

- Activate volume group
`vgchange -a y {{groupName}}`

- Create logical volume
`lvcreate -n {{volumeName}} -L {{size}} {{groupName}}`

- Show logical volumes
`lvdisplay`

- Increase size of logical volume
`lvextend -L +{{size}} {{/dev/groupName/volumeName}}`
