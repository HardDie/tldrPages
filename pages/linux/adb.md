# adb

> Adb

- List of attached devices
`adb devices`

- Run shell
`adb -s {{dev}} shell`

- List of packets
`pm list packages`

- Uninstall packet
`pm uninstall -k --user 0 {{packet}}`

- Restore packet
`cmd package install-existing {{packet}}`
