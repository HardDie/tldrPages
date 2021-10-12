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
