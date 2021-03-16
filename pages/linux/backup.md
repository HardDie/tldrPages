# backup

> Binary backup

- Create
`dd if={{/dev/sda}} | gzip -c > {{some.img.gz}}`

- Restore
`gzip -dc {{some.img.gz}} | dd of={{/dev/sda}}`
