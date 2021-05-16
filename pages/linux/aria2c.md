# aria2c

> Download application

- Download torrent file from magnet link
`aria2c --bt-metadata-only=true --bt-save-metadata=true {{link}}`

- Show files inside torrent file
`aria2c --show-files {{file.torrent}}`

- Download selected items from torrent
`aria2c --select-file {{1,3}} {{file.torrent}}`
