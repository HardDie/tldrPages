# go

> go usefull commands

- Flush test cache
`go clean -testcache`

- Generate profiles
`go test -bench=. -cpuprofile={{cpu.out}} -benchmem -memprofile={{mem.out}}`

- Run http pprof
`go tool pprof -http :{{9000}} {{cpu.out}}`

- Format time "YYYY-MM-DD HH:MM:SS"
`2006-02-01 15:04:05`
