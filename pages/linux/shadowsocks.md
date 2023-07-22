# shadowsocks

> How to use shadowsocks

- Start server
`go-shadowsocks2 -s 'ss://AEAD_CHACHA20_POLY1305:{{password}}@:8080' -verbose`

- Connect to server from client. Set in browser socks5 localhost:8080
`go-shadowsocks2 -c 'ss://AEAD_CHACHA20_POLY1305:{{password}}@{{host}}' -verbose -socks {{:8080}}`
