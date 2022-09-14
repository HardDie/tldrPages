# docker

> Docker usefull commands

- Set name for image
`docker image tag {{image_id}} {{name}}`

- Execute command inside container
`docker exec -it {{name}} {{command}}`

- Detach from container
`ctrl-p ctrl-q`

- Show logs
`docker logs {{container_id}}`

- Create network
`docker network create {{network-name}}`

- Add a container to the network
`docker network connect {{network-name}} {{container-name}}`
