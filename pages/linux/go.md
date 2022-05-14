# go

> go usefull commands

- Flush test cache
`go clean -testcache`

- Generate profiles
`go test -bench=. -cpuprofile={{cpu.out}} -benchmem -memprofile={{mem.out}}`

- Run http pprof
`go tool pprof -http :{{9000}} {{cpu.out}}`

- Format time "YYYY-MM-DD HH:MM:SS"
`2006-01-02 15:04:05`

- Register pprof
`routes := mux.NewRouter()`
`DebugRoute := routes.PathPrefix("/debug").Subrouter()`
`DebugRoute.HandleFunc("/pprof", http.HandlerFunc(pprof.Index))`
`DebugRoute.HandleFunc("/pprof/cmdline", http.HandlerFunc(pprof.Cmdline))`
`DebugRoute.HandleFunc("/pprof/profile", http.HandlerFunc(pprof.Profile))`
`DebugRoute.HandleFunc("/pprof/symbol", http.HandlerFunc(pprof.Symbol))`
`DebugRoute.Handle("/pprof/heap", pprof.Handler("heap"))`
`DebugRoute.Handle("/pprof/block", pprof.Handler("block"))`
`DebugRoute.Handle("/pprof/goroutine", pprof.Handler("goroutine"))`
`DebugRoute.Handle("/pprof/threadcreate", pprof.Handler("threadcreate"))`

- Determine which module use an indirect dependency
`go mod why -m {{module}}`

- Channel direction read/write
`ch <-chan int`
`ch chan<- int`

- Race detection
`go test -race {{main.go}}`
`go run -race {{main.go}}`
`go build -race {{main.go}}`
