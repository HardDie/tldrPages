# system

> Usefull command for system information

- Show boot log
`journalctl -b -p 3`

- Show poweroff log
`jour journalctl -b -1`

- Show full systemd process log
`journalctl -u {{name.service}}`

- Show all failed services
`systemctl --failed -all`

- Change console font
`pacman -S terminus-font`
`setfont {{ter-v32n}}`

- Change console font permanently
`echo "FONT={{ter-v32n}}" >> /etc/vconsole.conf`

- Check booting time
`systemd-analyze blame`
