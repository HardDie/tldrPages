# find

> Find util

- Rename files
`find -name '{{file.name}}' | xargs -I {} rename {{file.name}} {{new_file.name}} {}`

- Run command on every find file
`find -name "{{name}}" -execdir {{command}} {} \;`
