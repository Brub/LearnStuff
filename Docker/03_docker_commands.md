# Docker commands
[https://docs.docker.com/engine/reference/commandline/cli/](https://docs.docker.com/engine/reference/commandline/cli/0

## ps
the ps command will list all the containers

    docker ps

## run
The run command is to run a container frim an image. If the image is not available on the host, 
then the image will first be downloaded

    docker run <image>
## stop
this command will stop a comtainer

        docker stop <dockerName or dockerId>

## rm
the command will remove a contailer

        docker rm <dockerName>

## images
the command will list all the images of the host

        docker images
