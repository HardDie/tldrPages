# bash

> Bash

- Force varible declaration before access
`set -u`

- Make any failure in piped commands be reflected in the exit code
`set -o pipefail`

- Make fail script after error
`set -e`

- Remove current line in output
`echo -en \r`

- Is directory
`if [[ -d {{name}} ]]`

- Is file
`if [[ -f {{name}} ]]`

- Loop
`for {{val}} in {{{01..10};}} do {{echo $val;}} done`

- Loop array
`arr=("val1" "val2")`
`for val in ${arr[*]}; do echo ${val}; done`
