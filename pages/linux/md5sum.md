# md5sum

> md5sum

- Recusievly check md5 hash for all folders
`find -name {{checksum.md5}} -execdir md5sum --quiet -c {{checksum.md5}} \;`
