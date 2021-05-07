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

- Create patch file
`git diff --no-prefix > {{some.patch}}`

- Apply patch
`patch -p0 < {{some.patch}}`

- Create path file with prefix
`git diff > {{some.patch}`

- Apply path file with prefix
`patch -p1 < {{some.patch}}`

- Change commit author
`git commit --amend --author="{{Name}} <{{email}}>"`
