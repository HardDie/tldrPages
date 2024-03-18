# mysql

> MySQL info

- Get list of indexes for table
`SHOW INDEX FROM {{table}}`

- Info about table
`DESCRIBE {{table}}`

- Add index
`ALTER TABLE {{table}} ADD INDEX {{index_name_idx}} USING HASH ({{field}});`
