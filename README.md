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
- There are the following advantages of Docker -

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

