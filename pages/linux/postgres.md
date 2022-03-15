# postgres

> Postgres info

- Install fdw extension
`CREATE EXTENSION postgres_fdw;`

- Insert into table
`INSERT INTO {{table}} ({{column1}}, {{column2}}) VALUES ({{value1}}, {{value2}});`

- Create table from select
`CREATE TABLE {{new_table}} AS SELECT * FROM {{old_table}}`

- Create schema
`CREATE SCHEMA {{name}}`
`CREATE SCHEMA IF EXISTS {{name}}`

- Expand an array
`unnest({{array}})`

- Number of line
`SELECT row_number() OVER (), {{id}} FROM {{some.table}}`

- Update values
`UPDATE {{some.table}} SET {{column=value}} WHERE {{id=5}}`

- Create index
`CREATE INDEX {{index_name_idx}} ON {{some.table}} USING gin (lower({{field}}) gin_trgm_ops)`
`CREATE INDEX {{index_name_idx}} ON {{some.table}} ({{field}})`
`CREATE UNIQUE INDEX {{index_name_uidx}} ON {{some.table}} ({{field}})`

- Stop pid
`SELECT pg_cancel_backend({{pid}})`
`SELECT pg_terminate_backend({{pid}})`

- Disable pager
`\pset pager 0`

- FOREIGN KEY
`ALTER TABLE {{some.table}} ADD CONSTRAINT {{table_external_id_fkey}} FOREIGN KEY ({{external_id}}) REFERENCES {{parent_table(id)}}`
`ALTER TABLE {{some.table}} DROP CONSTRAINT {{table_external_id_fkey}}`

- Column
`ALTER TABLE {{some.table}} ADD COLUMN {{name INT}};`
`ALTER TABLE {{some.table}} DROP COLUMN {{name}};`
`ALTER TABLE {{some.table}} RENAME COLUMN {{name}} TO {{new_name}};`

- NOT NULL
`ALTER TABLE {{some.table}} ALTER COLUMN {{name}} SET NOT NULL;`
`ALTER TABLE {{some.table}} ALTER COLUMN {{name}} DROP NOT NULL;`

- Count elemnt by window function
`SELECT COUNT(*) OVER (PARTITION BY id) FROM {{some.table}}`
