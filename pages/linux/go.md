# go

> go usefull commands

- Flush test cache
`go clean -testcache`

- Generate profiles
`go test -bench=. -cpuprofile={{cpu.out}} -benchmem -memprofile={{mem.out}}`

- Run http pprof
`go tool pprof -http :{{9000}} {{cpu.out}}`
