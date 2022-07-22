# Dice Analytics DevOps Professional Training
## Batch No. 6 - Assignment No. 2

<br />

:bulb: **Question No. 1: Share the screenshot of the above Branch Protection of `main` branch.**

<br />

<img width="1431" alt="Screenshot 2022-07-22 at 6 40 51 PM" src="https://user-images.githubusercontent.com/101370133/180451492-c66bf213-cd03-470c-b9e6-b02130478c74.png">

---

<br />

:bulb: **Question No. 2: Explain Docker Containers vs VMs.**

<br />

| Differences | Docker Container | Virtual Machine (VM) |
| -- | -- | -- |
| Architecture | <img src=https://user-images.githubusercontent.com/101370133/180460388-5547b904-c021-4853-a6f7-7c0df0471919.png /> | <img src=https://user-images.githubusercontent.com/101370133/180460488-1469d57f-6577-4a8e-bf20-8821284c1b0f.png /> |
| Operating System | Docker is a container-based model where containers are software packages used for executing an application on any operating system.<br /><br />In Docker, the containers share the host OS kernel.<br /><br />Here, multiple workloads can run on a single OS. | It is not a container-based model; they use user space along with the kernel space of an OS.<br /><br />It does not share the host kernel.<br /><br />Each workload needs a complete OS or hypervisor. |
| Performance | Docker containers result in high-performance as they use the same operating system with no additional software (like hypervisor).<br /><br />Docker containers can start up quickly and result in less boot-up time. | Since VM uses a separate OS; it causes more resources to be used.<br /><br />Virtual machines don’t start quickly and lead to poor performance. |
| Portability | With docker containers, users can create an application and store it into a container image. Then, he/she can run it across any host environment.<br /><br />Docker container is smaller than VMs, because of which the process of transferring files on the host’s filesystem is easier. | It has known portability issues. VMs don’t have a central hub and it requires more memory space to store data.<br /><br />While transferring files, VMs should have a copy of the OS and its dependencies because of which image size is increased and becomes a tedious process to share data. |
| Speed | The application in Docker containers starts with no delay since the OS is already up and running.<br /><br />These containers were basically designed to save time in the deployment process of an application. | It takes a much longer time than it takes for a container to run applications.<br /><br />To deploy a single application, Virtual Machines need to start the entire OS, which would cause a full boot process.

---

<br />

:bulb: **Question No. 3: Explain Docker Architecture.**

<br />

Docker uses a client-server architecture. The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers. The Docker client and daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon. The Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface. Another Docker client is Docker Compose, that lets you work with applications consisting of a set of containers.

<br />

![architecture](https://user-images.githubusercontent.com/101370133/180474083-b9cf475c-7da1-481a-9ab7-215f5558282f.svg)

---

<br />

:bulb: **Question No. 4: Write command to create an nginx container in detached mode with name `assignment-2` running on host port `9090` and container port `80` on a custom network named `assignment-2`.**

<br />

```
docker run --name "assignment-2" -p 9090:80 -d nginx
```

---

<br />

:bulb: **Question No. 5: Write command to see logs of the above container.**

<br />

```
docker logs "assignment-2"
```

---

<br />

:bulb: **Question No. 6: Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html.**

```
docker exec "assignment-2" cat /usr/share/nginx/html/index.html
```

---

<br />

Done :tada: , Thanks for reading. :relaxed:
