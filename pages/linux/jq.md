# jq

> Json beautifier

- Format only json line, skip others
`jq -R -r '. as $line | try fromjson catch $line'`

- Ignore other lines
`jq -R 'fromjson?'`

- Print multiple fields
`jq -r '"\(.{{item1}}) \(.{{item2}})"'`

- Filter by field
`jq 'select(.{{field}} == "{{Value}}")'`
