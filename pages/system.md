# system

> Usefull command for system information

- Show boot log
`journalctl -b -p 3`

- Show all failed services
`systemctl --failed -all`

- Change console font
`setfont {{ter-v32n}}`

- Check booting time
`systemd-analyze blame`
