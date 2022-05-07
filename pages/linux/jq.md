# jq

> Json beautifier

- Format only json line, skip others
`jq -R -r '. as $line | try fromjson catch $line'`
