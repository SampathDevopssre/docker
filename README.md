# docker

### Container vs Docker

* Container is a package of your application.
* Docker is a container run-time to run the containers on linux machine. 

What is a container ?

Container is a package of software that contains all the required elements to run your applicaition in any environment


What is Run Time ?

To run containers, you need to have a run time and among all, DOCKER is highly used

How to run a container ?

$ docker run containerName    ( this runs containers interactively killing your prompt )
$ docker run -d containerName ( this runs containers in the background by detaching from the terminal )

Common docker commands:

$ docker images                      ( shows the list of container images available on your system)
$ docker ps                          ( shows you the list of all the running containers on your system )
$ docker ps -a                       ( shows you the list of all the containers including the exited ) 
$ docker pull imageName              ( pulls the docker image from the image repository )
$ docker push imageName              ( pushes the docker image to the image repository )
$ docker stop                        ( To stop the container which is running ) 
$ docker exec -it containerName bash ( To enter in to the container )


Port-Forwarding:

$ docker run -p 80:80  -d  nginx


Dynamic Porting:

docker run -P  -d httpd


Volume Mapping

docker run -v /home/verma/mysql-data:/var/lib/mysql  -e MYSQL_ROOT_PASSWORD=password -d mysql


ENTRYPOINT vs CMD

 The ENTRYPOINT specifies a command that will always be executed when the container starts. The CMD specifies arguments that will be fed to the ENTRYPOINT.
