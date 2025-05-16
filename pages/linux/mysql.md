# mysql

> MySQL info

- Get list of indexes for table
`SHOW INDEX FROM {{table}}`

- Info about table
`DESCRIBE {{table}}`

- Add index
`ALTER TABLE {{table}} ADD INDEX {{index_name_idx}} USING HASH ({{field}});`

- Group column
`SELECT {{id}}, GROUP_CONCAT({{value}}) FROM {{table}} GROUP BY {{id}}`

- Get first from array
`SELECT SUBSTRING_INDEX({{arr}}, ',', 1) FROM {{table}}`

- Get json value
`SELECT {{c}}, JSON_EXTRACT({{c}}, "$.{{id}}") FROM {{table}}`
