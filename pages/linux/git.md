# git

> Some usefull git commands

- Find removed string
`git log -S {{string}} {{file.c}}`

- Create empty commit
`git commit --allow-empty`

- Always create a merge commit
`git merge --no-ff`

- Remove local/remote branch
`git branch -d -r origin/{{branch}}`
`git push -d origin {{branch}}`

- Push local branch with different name
`git push origin {{localName}}:{{remoteName}}`

- Create patch file
`git diff --no-prefix > {{some.patch}}`

- Apply patch
`patch -p0 < {{some.patch}}`

- Create path file with prefix
`git diff > {{some.patch}}`

- Apply path file with prefix
`patch -p1 < {{some.patch}}`

- Change commit author
`git commit --amend --author="{{Name}} <{{email}}>"`

- Add submodule
`git submodule add {{url}} {{path}}`

- Rebase one branch to another
`git rebase {{branch}} {{move_branch}}`

- Create branch on commit
`git branch {{branch}} {{hash}}`

- Move branch to commit
`git branch --force {{branch}} {{hash}}`

- Remove local/remote tag
`git tag --delete {{tag}}`
`git push --delete origin {{tag}}`

- Remove file from git histor
`git filter-branch --index-filter 'git rm --cached --ignore-unmatch {{path/filename}}' {{first}}..HEAD`
