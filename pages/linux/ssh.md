# ssh

> SSH commands

- Copy ssh public key on remote server
`ssh-copy-id -i {{~/ssh/id_rsa.pub}} {{username}}@{{host}}`

- SSH tunnel: PC1 --> ( NAT ) --> WAN <-- PC2
`ssh -f -N -R {{PC2_PORT}}:{{PC1_IP}}:{{PC1_PORT}} {{PC2_name}}@{{PC2_IP}}`

- Run ssh-agent
`eval $(ssh-agent)`
`ssh-add ~/.ssh/{{id_rsa}}`
