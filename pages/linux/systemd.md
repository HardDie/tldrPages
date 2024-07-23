# systemd

> Info for PID 1 systemd

- Path where unit files stored
`/etc/systemd/system`
`/run/systemd/system`
`/lib/systemd/system`

- Edit unit file
`systemctl edit {{some.service}}`
`systemctl edit --full {{some.service}}`

- Reload unit files
`systemctl daemon-reload`
