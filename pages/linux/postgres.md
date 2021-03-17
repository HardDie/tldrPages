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
