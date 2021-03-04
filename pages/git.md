# git

> Some usefull git commands

- Find removed string
`git log -S {{string}} {{file.c}}`

- Create empty commit
`git commit --allow-empty`

- Always create a merge commit
`git merge --no-ff`

- Remove remote branch from local repository
`git {{branch}} -d -r origin/{{branch}}`

- Remove remote branch from remote repo
`git push -d origin {{branch}}`

- Push local branch with different name
`git push origin {{localName}}:{{remoteName}}`
