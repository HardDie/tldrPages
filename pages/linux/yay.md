# yay

> Usefull yay commands

- Show unused packets
`yay -Qdtq`

- Show explicitly installed packets
`yay -Qe`

- Show packets installed from AUR
`yay -Qm`

- Show packets installed from repository
`yay -Qn`

- Install packet as dependency
`yay -S {{packet}} --asdeps`

- Set install reason to dependency for packet
`yay -D --asdeps {{packet}}`