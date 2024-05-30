# sqlite

> SQLite info

- Enable foreign key
`PRAGMA foreign_keys = ON;`

- Check foreign key
`PRAGMA foreign_keys;`

- How to make backup
`sqlite3 {{my.db}} ".backup '{{mybackup.db}}'"`

- Enable displaying columns
`.headers ON`

- Align columns
`.mode columns`

- List of tables
`.tables`

- Show table description
`.schema {{table}}`
`PRAGMA table_info({{table}})`
