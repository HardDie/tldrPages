# user

> Usefull commands for work with user

- Create new user
`useradd -m -g users -G wheel {{username}}`

- Add user to group
`usermod -a -G {{groupname}} {{username}}`

- Show active user groups
`groups`
