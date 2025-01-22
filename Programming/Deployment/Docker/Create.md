#### Build Docker image from file
`docker build <--no-cache> <-t [my-name]> <dir>` ^9dbc78

#### Make and run docker container from [image](Create.md#^9dbc78)
docker run <--name [docker-container-name]> <--network [network-name](Create.md#^c70113)> <-d> <-p [external-`port:internal-port]> <image-id>` ^8ae559

#### Create a Docker Network
`docker network create <network-name>` ^c70113

