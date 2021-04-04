# iptables

> Useful iptables commands

- Set TTL to 65 for output packages
`iptables -t mangle -A POSTROUTING -o {{interface}} -j TTL --ttl-set 65`

- Setup NAT
`echo net.ipv4.ip_forward = 1 >> /etc/sysctl.d/99-sysctl.conf`
`iptables -t nat -A POSTROUTING -o {{interface}} -j MASQUERADE`

- LOG packages
`iptables -A INPUT -j LOG --log-prefix "PREFIX: "`

- Accept packets only from IP:PORT
`-A INPUT -i {{interface}} -p {{tcp}} -m {{tcp}} --dport {{PORT}} -s {{IP}} -j ACCEPT`
