what is a container 
is a way to package applications with all the necessary dependencies and configuration 
- it is a portable artifact easily shared and moved around
- containers live in a container repository 
- many companies have private repositories to store containers.
- there is also public repository for docker e.g docker hub (it contains images like jenkins , alpines, node ...)

how do containers use
when there is 
- installation process difference on each os environment
- many steps to install
-but containers solve this 
In Application development

    -having own isolated environment 
     -packaged with all needed configuration 
     -one command to install the app 
     - run the same application with 2 versions 
In Application Deployment   
     -when configuration on the serer needed 
         -dependency version conflicts
     -textual guide of deployment
          -misunderstandings
    developers and operations work together to package the application in a container
     no environmental configuration needed on server . except docker runtime
 -technically container is made up of images 
 -mostly linux base image , becase small in size 
 -docker containers are made up of layers that layers are separately run.

Docker Image 
- the actual package 
- artifact, that can be moved around 

Docker vs virtual machine 

-os contains 2 layers application and os kernel
- docker virtualizes the application system 
-vitual machine is for os kernel 

docker - small size 
       - fast to run  than vm 

*the difference between image and container*
- container is a running environment for image
*container port vs host port
*some docker commands 
docker start = to start a container 
docker stop = to stop a container 
docker images= to see local images 
docker ps = to see which images are runing 
docker logs (container id)= to troubleshooting
docker run = when we create a new containers from image(it used to create a container)
docker start = when the container once created we use docker start to start a stopped container 


docker network 
when we deploy two containers in the same docker network e.g mongo and mongo express  they can talk to each other using just the container name with out localhost, port no ...because they are in the same network. but if it is out side docker network (host) it is connected by localhost and port number 

*docker compose *

- docker run command 
`docker run -d --name (name ) -p (port:port) -e mongo-initdb-username=(username) -e mongo-INITDB_ROOT_PASSWORD=(password) --net (networkname)  (imagename)`

if we have to connect many containers then we have write a docker run command for all of them which is boring 
docker compose is a structured way to run docker run commands in easier way. if we wanna change any info it is easier .
*Docker compose takes care of creating a common network .*
- docker compose command 
-mongo-docker-compose.yaml
`version:3
`services:
`mongodb:
     `image:mongo
     `ports:2017:2017
     `environment 
     ` 
     docker compose command 
     `docker compose -f mongo.yaml up` =to start 
    `docker compose -f mongo.yaml up= to stop 
 logs of container mixed in case of docker compose
 - there is no data persistence in containers data lost when we restart.

Docker file 

- a blueprint for building docker image 
- example 
-image environment blueprint  vs DOCKERFILE
 - install node           ==FROM node 
 - set mongo_db_USERNAME=admin  ==ENV mongo_db_USERNAME=admin 
 - create /home/app folder  ==RUN mkdir -p home/app
 - copy current folder files to /home/app ==COPY . /home/app
 - start the app with :"node server.js" ==CMD ["node","server.js"]
- cmd is just entrypoint command 
- but run can have multiple command 

to create docker image from docker file 
 `docker build -t my-app:1.0 .`
\
Docker volume 

used for data persistent 
for docker container if it restart the data lost.
data gets automatically replicated from virtual file system to host file system (physical)

volume types 
1.host volume 
- created by docker run command 
- -v (to define path of host directory )
- in this volume you decide where on the host file system the reference is made.e.g
- like /home/app/.....
2.Anonymous volume 
- created just by referencing 
- for each container a folder is generated that gets mounted. e.g
- like  /var/lib/mysql/data
3.Named volume 
- you can reference the volume just by name e.g 
- -v (name):/var/lib/mysql/data