# postgres

> Postgres info

- Install fdw extension
`CREATE EXTENSION postgres_fdw;`

- Insert into table
`INSERT INTO {{name}} (id, title) VALUES ({{id}}, {{title}});`

- Create table from select
`CREATE TABLE {{new_table}} AS SELECT * FROM {{old_table}}`

- Create schema
`CREATE SCHEMA {{name}}`
`CREATE SCHEMA IF EXISTS {{name}}`
