## What is Docker ?

> **Docker is a Containerization Platform which allows us to containerize an application/software (called as Docker Image) & also lets you run Containerized application/software**

> **Technical Deffinition:**

> Docker is an open source software platform to create, deploy and manage virtualized application containers on a common operating system (OS), with an ecosystem of allied tools.

> Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers.

## Docker Architecture 

### `Docker Engine`

> Have you tried to install Docker yet? You might have noticed that you’re required to install not just Docker, but also something called dockerd.

> That is because Docker is a client-server application. You must have both parts for running a Docker application on your computer. This client-server tandem is called docker engine.

> The docker client is just a CLI tool to make requests against a REST API, which is responsible for interacting with the docker daemon or dockerd. dockerd will deal with the operative system to ensure the proper behaviour for the containers.

![Docker Engine Flow](https://github.com/lerndevops/slearncka/blob/master/static/docker-engine-components-flow.png)

> Now we have a clear understanding of the main elements of Docker, how does it all work together

> Whenever a request is created in the Docker client, it’s sent to the Docker daemon and it will perform the required actions.

> Let’s use as an example running a redis container. We achieve that by running the instruction docker run redis.

> First, our computer will make a request to the configured docker host API, which is going to interact with the Docker daemon.
At this point, the daemon knows what it must do. It will look up the redis image on the host registry. If it’s not present, a new lookup will be made, this time against the configured image registry (Docker Hub, ECR, ACR, GCR, …) and pulled (downloaded). Then it will spawn a container based in the downloaded image.

![Docker Architecture](https://github.com/lerndevops/slearncka/blob/master/static/Docker-architecture.png)


## what is Docker Image ?

> A package which consists of an application/software with all its dependencies to run, **Called as Docker Image**

> Docker Image will have a base layer of minimal OS in it always, on top of OS layer we install software & its dependenci
es.

> A Docker image is built up from a series of layers. Each layer represents an instruction that we run.

> A Docker image is a lightweight, standalone, executable package of software that includes everything needed to run an a
pplication: code, runtime, system tools, system libraries and settings

> Docker Images are immutable

> Images are stored in a Docker registry such as registry.hub.docker.com

## what is Docker Container ?

> A container is runtime instance of a Docker Image

> A Container is the actual instantiation of the image just like how an object is an instantiation or an instance of a cl
ass.


## Advantages of Containers

#### Physical vs. Virtual Machines vs. Container


| Physical | Virtaul Machines | **Containers** |
| :-------- | :-------------- | :---------- |
| No virtualization | H/W level virtualization | **OS level Vertualization** |
| Huge Maintenance Cost | Huge Maintenance Cost | **No Maintenance Cost** |
| No Scalability | Scalability is Hard | **Easily Scalable** |
| Huge Resource Wastage | Better Resource Usage but Dynamic Allocation is NOT Possible | **Dynamic Resource Allocation is
 Possible** |
| Takes Longer Time to Initialize App (boot time) | Almost Same as Physical  | **Take Very Less Time to Initialize App (l
ess boot time)** |
