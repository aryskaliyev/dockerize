### Docker

Docker is an open-source platform that allows you to *automate the deployment and management of applications* within lightweight, isolated containers. It provides a consistent environment for running software, regardless of the underlying infrastructure.

![Docker](img/docker2.png)

###### Here are some key concepts and components of Docker:

1. **Containers**:\
Docker uses containers to encapsulate applications and their dependancies. A container is a *running instance of an image*. A container is a lightweight, standalone *executable package* that includes everything needed to run an application, such as code, runtime, system tools, libraries, and settings.

2. **Images**:\
Containers are created from Docker images. An image is a *read-only template* that contains the instructions for creating a container. It includes the application code and all the dependencies needed to run the application. Images can be built from scratch or based on existing images available on Docker Hub or private repositories.

3. **Docker Engine**:\
Docker Engine is the *runtime* that enables the creation and execution of containers. It manages the container lifecycle, including starting, stopping, and monitoring containers. Docker Enginer runs on the host machine and provides an API and command-line interface (CLI) to interact with Docker.
 
4. **Dockerfile**:\
A Dockerfile is a text file that contains a set of instructions for building a Docker image. It specifies the base image, software dependencies, configuration settings, and commands needed to create the image.

5. **Docker Compose**:\
Docker Compose is a tool for defining and running multi-container Docker applications. It uses a YAML file to define the services, networks, and volumes required by an application. Compose simplifies the process of managing complex, interconnected containers as a single unit.

6. **Docker Registry**:\
Docker Registry is a repository for storing and distributing Docker images. *Docker Hub* is the default public registry provided by Docker, but you can also set up private registries to store images within your organization.

7. **Orchestration**:\
*Docker Swarm* and *Kubernetes* are popular orchestration platforms that allow you to manage and scale Docker containers across a cluster of machines. They provide features like container schedulling, load balancing, service discovery, and automaged scaling.

###### Benefits of using Docker:

- **Portability**:\
Docker containers provide a consistent environment, making applications easily portable across different machines, operating systems, an cloud platforms.

- **Scalability**:\
Containers can be scaled up or down quickly to handle varying workload demands. Docker Swarm and Kubernetes provide tools for orchestrating containerized applications at scale.

- **Isolation**:\
Containers provide process isolation, ensuring that applications run independently without interfering with each other or the underlying system.

- **Resource efficiency**:\
Containers are lightweight, as they share the host system's kernel, enabling more efficient resource utilization compared to virtual machines. 

- **Rapid deployment**:\
Docker simplifies the application deployment process by packaging the application and its dependencies into containers, allowing faster and more reliable deployment.

###### Commands:

- `docker images` = List all Docker images.
- `docker ps` = List running containers.
- `docker pull {image-name}` = Pulling image {image-name} from Docker Hub.
- `docker run {image-name}:{image-tag}` = Creates a container from given image and starts it. Creates a new container. Doesn't re-use previous container.
	- `-d` or `--detach` = Runs a container in background and prints the container ID.
	- `-p {HOST_PORT}:{CONTAINER_PORT}` or `--publish {HOST_PORT}:{CONTAINER_PORT}` = Publish a container's port to the host.
- `docker logs {container-ID}` = View logs from service running inside the container (which are present at the time of execution).
- `docker stop {container-ID}` = Stop one or more running containers.
