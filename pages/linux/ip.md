# ip

> Useful ip commands

- Remove default gw
`ip route del default via {{192.168.1.1}}`

- Add route
`ip route add {{192.168.2.0/24}} via {{192.168.1.1}} dev {{enp3s0}}`
