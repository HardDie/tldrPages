# vim

> Usefull vim info

- Fold lines
`zf va {{}/]/)}}`
`:{range}fo`

- Unfold
`zd`

- Count selected lines
`g C-g`

- Increase / decrease number
`C-a`
`C-x`

- Set syntax
`set syntax={{type}}`

- Move tab
`:tabm {{1}}`

- Split vertical/horizontal
`ctrl+w s`
`ctrl+w v`

- Sort selected lines (straight, reverse, unique, numeric)
`:sort`
`:%sort!`
`:%sort u`
`:sort n`

- Run without plugins
`vim -u NONE {{file}}`
