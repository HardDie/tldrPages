# system

> Usefull command for system information

- Show boot log
`journalctl -b -p 3`

- Show all failed services
`systemctl --failed -all`

- Change console font
`pacman -S terminus-font`
`setfont {{ter-v32n}}`

- Change console font permanently
`echo "FONT={{ter-v32n}}" >> /etc/vconsole.conf`

- Check booting time
`systemd-analyze blame`
