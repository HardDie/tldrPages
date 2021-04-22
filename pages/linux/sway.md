# sway

> Sway useful commands

- Run in debug mode
`sway -d 2> {{~/sway.log}}`

- Get color from screen
`grim -g "$(slurp -p)" -t ppm - | convert - -format '%[pixel:p{0,0}]' txt:-`

- List active windows
`swaymsg -t get_tree`

- Reload
`swaymsg reload`

- Exit
`swaymsg exit`
