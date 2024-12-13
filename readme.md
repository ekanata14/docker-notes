# Docker notes
Reference: https://youtu.be/3_yxVjV88Zk?si=4yeCD35HTwzO9CJK

## Docker Image
Docker Image is something that is a package for the container. It contains thing like nginx, node or anything else that is needed for the container

### Docker Image Command

Show all images
- docker image ls

Pull a package or image from docker hub
- docker image pull packagename:version (redis:latest)

Remove docker image
docker image rm packagename:version (redis:latest)

### Docker Container
Docker container is something that isolate our images. It contains our system, package and anything else that is needed to run the application

Show all conatainers
- docker container ls

Create docker container
- docker container create --name examplename packagename:latest (redis:latest)

Start a docker container
- docker container start examplename

Stop a docker container
- docker container stop examplename


Remove/delete a docker container
- docker container rm examplename


### Docker Log
Log for docker container to see how the container runs and see some errors.

Show docker container logs
- docker container logs examplename

Watching docker container logs realtime
- docker container logs -f examplename

### Docker Exec
When we wanna access application that only contain inside the container, we can use docker exec to access it. For example, we wanna access the terminal from the container we run. Use docker exec. We use bash scripting to access it

The command:
- docker container exec -i -t examplename /bin/bash

Notes:
    -i : keep interactive argumentand keep the input stay activated
    -t : Psuedo-TTY terminal access
    /bin/bash : Example for the program we'd like to access inside the container


