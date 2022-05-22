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

Most of conatiner images have OS LAYER at the bottom and application layer at the top most. 

1. Downloading images in layers is easy
2. Most important benefit of using layers is time efficient. Suppose we already have one container runnig and we have to download the latest image of that container, then layers which are new only will be downloaded. Layers which are common in old and new version will not be downloaded.


### INSTALLATION OF DOCKER

* Download the docker package from docs.docker.com OR search google to install the docker
* docker usually creates a group by default with named 'docker'
* Provide the docker GID to the user with which you will do configuration for containers

>DOCKER COMMANDS

** docker version 			Version of docker
** docker pull image			Pull image from docker hub.
