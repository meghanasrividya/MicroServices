# MicroServices

### What are Microservices?

- Microservices are an architectural and organizational approach to software development where software is composed of small independent services that communicate over well-defined APIs. These services are owned by small, self-contained teams.

Microservices architectures make applications easier to scale and faster to develop, enabling innovation and accelerating time-to-market for new features.

### Benefits of Microservices:

- Agility
- Flexible Scaling
- Easy Deployment
- Technological Freedom
- Reusable Code
- Resilience

### Differences between monolith and microservices

- Monolithic vs. Microservices Architecture
With monolithic architectures, all processes are tightly coupled and run as a single service. This means that if one process of the application experiences a spike in demand, the entire architecture must be scaled. Adding or improving a monolithic application’s features becomes more complex as the code base grows. This complexity limits experimentation and makes it difficult to implement new ideas. Monolithic architectures add risk for application availability because many dependent and tightly coupled processes increase the impact of a single process failure.

- With a microservices architecture, an application is built as independent components that run each application process as a service. These services communicate via a well-defined interface using lightweight APIs. Services are built for business capabilities and each service performs a single function. Because they are independently run, each service can be updated, deployed, and scaled to meet demand for specific functions of an application.

![image](https://user-images.githubusercontent.com/97250268/203053771-ddc1ff7e-43df-48e6-8165-82374d8290b6.png)


### What is Docker?

- Docker is an open source platform that enables developers to build, deploy, run, update and manage containers—standardized, executable components that combine application source code with the operating system (OS) libraries and dependencies required to run that code in any environment.
### Why use Docker?
- Docker is designed to benefit both the Developer and System Administrator. There are the following reasons to use Docker -

- Docker allows us to easily install and run software without worrying about setup or dependencies.
- Developers use Docker to eliminate machine problems, i.e. "but code is worked on my laptop." when working on code together with co-workers.
- Operators use Docker to run and manage apps in isolated containers for better compute density.
- Enterprises use Docker to securely built agile software delivery pipelines to ship new application features faster and more securely.
- Since docker is not only used for the deployment, but it is also a great platform for development, that's why we can efficiently increase our customer's satisfaction.

### Advantages of Docker
- These are the following advantages of Docker -

- It runs the container in seconds instead of minutes.
- It uses less memory.
- It provides lightweight virtualization.
- It does not a require full operating system to run applications.
- It uses application dependencies to reduce the risk.
- Docker allows you to use a remote repository to share your container with others.
- It provides continuous deployment and testing environment.

### Docker Engine:
- It is a client server application that contains the following major components.
- A server which is a type of long-running program called a daemon process.
- The REST API is used to specify interfaces that programs can use to talk to the daemon and instruct it what to do.
- A command line interface client.

![image](https://user-images.githubusercontent.com/97250268/203069350-b7a2321e-016d-4f4d-9fe5-6d350d1d060b.png)

## Docker Architecture

![image](https://user-images.githubusercontent.com/97250268/203145602-b5b60d02-2956-48fc-be79-e4657c72ee0b.png)

## Container Life Cyle

![image](https://user-images.githubusercontent.com/97250268/203145264-a1849ddb-6d0b-485f-816b-d99bfa59d178.png)



### Differences between containers and virtual machines
![image](https://user-images.githubusercontent.com/97250268/203070410-b44d743e-fdf7-4a02-8225-1323163909e1.png)

`alias docker="winpty docker"`

### Docker Commands
```

Usage:  docker [OPTIONS] COMMAND

A self-sufficient runtime for containers

Options:
      --config string      Location of client config files (default
                           "C:\\Users\\MA\\.docker")
  -c, --context string     Name of the context to use to connect to the
                           daemon (overrides DOCKER_HOST env var and
                           default context set with "docker context use")
  -D, --debug              Enable debug mode
  -H, --host list          Daemon socket(s) to connect to
  -l, --log-level string   Set the logging level
                           ("debug"|"info"|"warn"|"error"|"fatal")
                           (default "info")
      --tls                Use TLS; implied by --tlsverify
      --tlscacert string   Trust certs signed only by this CA (default
                           "C:\\Users\\MA\\.docker\\ca.pem")
      --tlscert string     Path to TLS certificate file (default
                           "C:\\Users\\MA\\.docker\\cert.pem")
      --tlskey string      Path to TLS key file (default
                           "C:\\Users\\MA\\.docker\\key.pem")
      --tlsverify          Use TLS and verify the remote
  -v, --version            Print version information and quit

Management Commands:
  builder     Manage builds
  buildx*     Docker Buildx (Docker Inc., v0.9.1)
  compose*    Docker Compose (Docker Inc., v2.12.2)
  config      Manage Docker configs
  container   Manage containers
  context     Manage contexts
  dev*        Docker Dev Environments (Docker Inc., v0.0.3)
  extension*  Manages Docker extensions (Docker Inc., v0.2.13)
  image       Manage images
  manifest    Manage Docker image manifests and manifest lists
  network     Manage networks
  node        Manage Swarm nodes
  plugin      Manage plugins
  sbom*       View the packaged-based Software Bill Of Materials (SBOM) for an image (Anchore Inc., 0.6.0)
  scan*       Docker Scan (Docker Inc., v0.21.0)
  secret      Manage Docker secrets
  service     Manage services
  stack       Manage Docker stacks
  swarm       Manage Swarm
  system      Manage Docker
  trust       Manage trust on Docker images
  volume      Manage volumes

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  build       Build an image from a Dockerfile
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  events      Get real time events from the server
  exec        Run a command in a running container
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  images      List images
  import      Import the contents from a tarball to create a filesystem image
  info        Display system-wide information
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  login       Log in to a Docker registry
  logout      Log out from a Docker registry
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  ps          List containers
  pull        Pull an image or a repository from a registry
  push        Push an image or a repository to a registry
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  run         Run a command in a new container
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  search      Search the Docker Hub for images
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  version     Show the Docker version information
  wait        Block until one or more containers stop, then print their exit codes


```
- Docker images: Will present the images available
- Docker ps: To check the containers running
- Docker ps -a: To check every container running including hidden files
- Docker pull: to pull the image from docker hub
- Docker run : to run the image live directly from dockerhub
- docker exec -it [container id] bash: to access the running container
- docker stop: stops a running container
- docker kill: kills container by stopping execution. stop gives time to shut down gracefully
- docker commit [container id][username/imagename]: creates new image of an edited container on local system
- docker rm [container id]:removes container
- docker history [image name]: to view history
- docker image rm [image name]: deletes image
- Making docker docs available on our localhost
- docker run -d -p 4000:4000 docs/docker.github.io for docker documentation
- Logging into a running container
- docker exec -it <container-id/name> sh
- Port mapping in our containers with localhost
- docker run -d -p localhost-port:container-port
- Copying files to container
- docker cp <container_id>:path/to/file
- Running a container with ghost
- docker run -d -p 2368:2368 ghost
- Running nginx on port 80
- docker run -d -p 80:80 nginx

## Replacing the nginx home page with CV:

- /usr/share/nginx/html has nginx web files

- Can replace index.html to alter website appearance
- Create index.html of your CV
- Copy the index.html to the same place/folder where nginx index.html is stored
- Open your GitBash as admin and give this command `$ docker cp index.html  795c688a6300:/usr/share/nginx/html `, this will copy the index.html from local host to container
- You can see your CV on browser
![image](https://user-images.githubusercontent.com/97250268/203118954-d5aabd03-9bbb-4978-8090-f7a7d5a28054.png)

## Build the docker image
- `$ docker build -t meghanasrividya/my-page:meghana`
- `$ docker tag nginx meghanasrividya/my-page:meghana`
- `$ docker commit 795c688a6300 meghanasrividya/my-page:meghana` # creates image in local system

![image](https://user-images.githubusercontent.com/97250268/203122086-3282eaed-f55d-4dd5-bf19-50ec1c582fb1.png)

## Push to the dockerhub

- `$ docker push meghanasrividya/my-page:meghana`


![image](https://user-images.githubusercontent.com/97250268/203145845-dca59abe-66a6-41d9-9559-6b597b7c50a8.png)

## Automate the process of building image
- Create the Dockerfile at the same location as your index.html
```
# docker run nginx

FROM nginx

# who is creating this

LABEL MAINTAINER=ameghana



# created index.html profile -copy to container

COPY index.html /usr/share/nginx/html/
# default location /usr/share/nginx/html

# docker run -d -p 80:80 name

# port number
EXPOSE 80

# launch the server
CMD ["nginx", "-g", "daemon off;"]





```
## Node App Task
- Create a new folder and copy app and environment folders inside
- `mkdir eng130-node`
- Create the Dockirfile `nano Dockerfile` and add the below script
 ```
 FROM nginx
LABEL MAINTAINER=Meghana
COPY app/ /home/
EXPOSE 80
EXPOSE 3000
RUN apt-get update
RUN apt-get install -y
RUN apt-get install software-properties-common -y
RUN apt-get install npm -y
CMD ["nginx", "-g", "daemon off;"]
WORKDIR /home/app
RUN npm install
CMD ["npm", "start"]



 ```
 
 - To Build the image use the command `$ docker build -t meghanasrividya/eng130-nodeapp .` 
 - To run the image use the command `$ docker run -d -p 3000:3000 meghanasrividya/eng130-nodeapp`
 - We can see the app running at `localhost:3000` in browser
 
 ![image](https://user-images.githubusercontent.com/97250268/203329362-ac1a22ee-c5f1-4d85-ad77-9d3e3d71df2f.png)

 - To push to the docker hub `$ docker push meghanasrividya/eng130-nodeapp`

## What is Docker Compose?

- Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application's services.

## Create a .yml file with docker-compose to launch our app with mongodb

- `nano docker-compose.yml` 

```
version: '3'

services:
  # start the db image and map to port 27017
  db:
    image: mongo
    restart: always
    ports: [27017:27017]
    volumes:
    - data-volume:/data/db
    - ./mongod.conf:/etc/mongod.conf

  web:
    # start up the web app image and map to localhost
    build: ./app
    restart: always
    ports: [80:3000]
    # set variable for a db port
    environment:
      - DB_HOST=mongodb://db:27017/posts
    depends_on:
      - db
    volumes:
    - ./app:/src/app
    # could also use links
    # can run the seeds here if CMD doesn't work
     
    
volumes:
  data-volume:
```
