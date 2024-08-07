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

- List of networks
`docker network ls`

- Create network
`docker network create {{network-name}}`

- Add a container to the network
`docker network connect {{network-name}} {{container-name}}`

- How to save changed container
`docker commit {{container_id}} {{new_image_name}}`

- How to login on private repository
`docker login`

- Clean build cache
`docker builder prune`
