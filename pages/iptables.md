# iptables

> Useful iptables commands

- Set TTL to 65 for output packages
`iptables -t mangle -A POSTROUTING -o {{interface}} -j TTL --ttl-set 65`

- Setup NAT
`iptables -t nat -A POSTROUTING -o {{interface}} -j MASQUERADE`
