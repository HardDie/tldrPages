# rsync

> Usefull rsync commands

- How to sync music
`rsync -cvr --stats --progress --delete --exclude={{Covers}} {{sourceDir}}/* {{destinationDir}}`

- How to sync via ssh
`rsync -avz -e 'ssh -p {{22}}' --progress {{IP}}:{{destinationDir}} {{sourceDir}}`
