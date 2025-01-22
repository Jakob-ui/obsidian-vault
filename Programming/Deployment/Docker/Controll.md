##### Start specifc container (it has to be [built from image](Create.md#^8ae559) first)
`docker start <container-name/container-id>`

##### Stop specifc container (it has to be [built from image](Create.md#^8ae559) first)
`docker stop <container-name/container-id>` ^511183

#### Stop every running container
`docker stop $(docker ps -q)`