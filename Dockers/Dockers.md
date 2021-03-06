#          DOCKERS	

### Difference in Container & Virtual Machine

- Docker Containers are very less in size whereas VMs are in GBs
- Docker Containers start and run much fast as compare to VMs
- A disadvantage of using Docker container is that image of particular OS might not be compatible with other operating system. So, before using the container image first step is to check if the container image is compatible with the native machine Operating System. To overcome these limits we can use docker tools/desktop.


### What is Container

A way to package the application with ALL DEPENDENCIES which application require to run is called CONTAINER. 

* Containers are PORTABLE
* Efficient
* Different version of same application can run on same machine

### Difference in Container Image and Container

A container image which we download from repository is called image. its a package which has application and all its dependencies.
-	Image can be moved around between system and different repositories.

When we download the image and install it on system, its called as Container. 
- When we install the image and running the application on system, then its called as Container. Containers are running images and can't be moved around.
- Containers have a binded port through whcih tahye talk to applicatiion running inside the
- Containers have VIRTUAL FILESYSTEM



### Repositories
Cotainer Images are found in repositories. We have two types of repositories:
					
	**Private Repositories** (Many companies have maintain their own repositories on their infrastructure or public/private cloud)
		
	**Public Repositories** (shared with public, like DOCKERHUB)


### Before and after Containers

##### Before
1. Running application on on-premise infrastructure was costly
2. Lots of dependency was on OS
3. Running different version of application was difficult
4. Developers, DBAs, OS admins were all separate

##### After
1. Different version of application/service can be run on same system now
2. Own isolated environment is possible
3. Easy to run application, even sometime using script its a few second task to setup new application
4. A new profile have originated, DevOps. 
5. No enviornment configuration require on server

### Container Layers
Container Images are consist of layers. These layers include multiple libraries which are require to run the service. 

Stackable Unification File System ( Unionfs) is used to create Docker images. Unionfs is 

Most of container images have OS LAYER at the bottom and application layer at the top most. 

1. Downloading images in layers is easy
2. Most important benefit of using layers is time efficient. Suppose we already have one container runnig and we have to download the latest image of that container, then layers which are new only will be downloaded. Layers which are common in old and new version will not be downloaded.

### <span style="color:Yellow">DOCKER ARCHITECTURE</span>

![Architect](Images/Architect.JPG)

Docker engine consists of several components as shown in figure. Client and Server run simultaneously on the same host. 

Client communicates with the server using a REST API which enables the client to also communicate with a remote server instance. 

##### Docker Client 
Its a CLI application named as "docker". it provides us CLI to interact with a docker server. It uses REST API to send instructions to either a local or remote server.

##### Docker Server
Its a daemon - 'dockerd'. Again it uses instructions sent by docker REST API and can interact with other daemons. 

### <span style="color:Yellow">INSTALLATION OF DOCKER</span>

* Download the docker package from docs.docker.com OR search google to install the docker
* docker usually creates a group by default with named 'docker'
* Provide the docker GID to the user with which you will do configuration for containers

>DOCKER COMMANDS

| COMMAND               | PURPOSE OF COMMAND         |
|-----------------------| ---------------------------|
| docker version		| print the current docker version|
|docker images			| List all current images in current system|
| docker pull <\image>  | pull image from docker hub |
| docker run <\image>	| install the image 		  |
| docker ps				| list running containers on system |
| docker run -d <\image> | install the image in DETACH MODE |
| docker ps -a 			| list all containers running and stopped |
| docker run <\image.version> | download the package from docker hub and install the image | 
| docker run -p6000:27001 <\image>| start the container and bind the container port to system port 6000 |
| docker run -d -p6000:12433 --name <\docker_name> <\image> | to provide customize name to docker |
| docker exec -it <\container> /bin/bash | take terminal console of container. here it stands for interactive terminal |
| docker rmi <\image> | delete the image | 
| docker stop <\container> | stop the container |
| docker start <\container> | start the container |
| docker network ls | list network names withing container | 
| docker logs <\container> | check container logs | 
| docker tag tag_name <\image> | tag the image |
| docker push |  push the image to docker hub | 


### <span style="color:Yellow">DOCKER NETWORK</span>

DOCKER creates its on virtualize network through which containers talk to each other.

* containers can talk to each other without any port
* But outside network/machines can talk to these containers using port only

![Image](Images/Capture.JPG)


| COMMAND               | PURPOSE OF COMMAND         |
|-----------------------| ---------------------------|
|docker network ls| list the existing container network|
| docker network create <\network-name> | create the network |


