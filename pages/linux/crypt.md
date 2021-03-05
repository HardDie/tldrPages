# crypt

> Information about HDD encryption

- Encrypt disk
`cryptsetup luksFormat {{/dev/sda2}}`

- Open encrypted disk
`cryptsetup open {{/dev/sda2}} {{name}}`
