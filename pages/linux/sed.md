# sed

> How to use regexp

- Replace text and keep value between
`sed -E -e 's/""(.*)""/"\1"/g'`

- Replace Uppercase with lowercase
`sed 's/[A-Z]/\L&/g'`

- Replace lowercase with Uppercase
`sed 's/[a-z]/\U&/g'`
