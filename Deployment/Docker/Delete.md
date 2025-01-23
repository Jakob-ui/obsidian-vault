#### Delete distinct thing
`docker rm <container-id>`
`docker rmi <image-id>`

#### Delete all images (only when [all containers are stopped](Controll.md#^511183))
`docker image ls -q | ForEach-Object { docker image rm $_}`
*optional use <-f> tag to force delete*