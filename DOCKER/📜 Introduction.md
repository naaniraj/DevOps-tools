# 🚢docker 🐳
********************

![![Docker-Architecture (1)](https://github.com/user-attachments/assets/be158689-f395-47cf-aa7f-c02d247ece01)
)

## 🚢 Docker Components :-

 - when we run the cammand its will check is thare that image in our local or not<br>
   then it will go to docker host and gave the our required image<br>
   if stil thare is no image in docker host it will give from docker regestry to docker client .<br>
   
## What is DOCKER ?
******************************
Docker is a tool that helps you build, package, and run applications easily.  it like a container
that holds everything your application needs—code, libraries, and dependencies—so it runs the same way everywhere,
whether on your laptop, a server, or in the cloud.

* when we wanna run the application it's won't support all operating system <br>
so we use containers to run in diffrent operating system <br>
so we use mltiple containers in our application to work multiple OS 

Just like a shipping container that can be moved from one place to another
without worrying about what's inside, Docker ensures your application works the same way, no matter where you run it.

### 1. 𝗪𝗵𝗮𝘁 𝗶𝘀 𝗗𝗼𝗰𝗸𝗲𝗿? 
*******************************
 Docker is a platform that automates the deployment of applications inside lightweight,
 portable containers, easing the software deployment process.

### 2 .What is a container?
**********************************
A container is an isolated environment that packages an application and all its dependencies, 
ensuring it runs consistently across different environments

### 3 .What is the difference between a container and a virtual machine?
*******************************************************************
 1 - resouce utalization ----  Containers are more lightweight than virtual machines because they share the host system’s kernel,
                                while virtual machines have their own separate operating systems.📦 (V / M) -- its have full fledge operation system 
                                and hyper version ,making then more resouce-intensive .
                                
 2 - portabulity ------------- containers disigend for to portable for run any operating system with compatable host operating system 
                              📦 ( V / M) -- are less portable as they need .

 3 - Security  --------------  containers provide less isolation as per share the operating system 
                              📦 ( V / M ) --  provide higher level security as each V/M have a own operating system 
                               and it can be isolated from other host and other V/M

 4 - management ------------- managing  containers are easy then managing 📦v/m  we can use whare ever you want .   

 ## 🚢-DOCKER - CONCEPT
**********************

•𝗜𝗺𝗮𝗴𝗲𝘀<br>
↳ Read-only templates that are used to build containers. Images are created with Dockerfile instructions or can be downloaded from a Docker registry like Docker Hub.

𝗖𝗼𝗻𝘁𝗮𝗶𝗻𝗲𝗿:<br>
↳ An instance of an image. It's a lightweight, standalone package that includes everything needed to run an application.

𝗗𝗼𝗰𝗸𝗲𝗿𝗳𝗶𝗹𝗲<br>
↳ A script-like file that defines the steps to create a Docker image.

𝗗𝗼𝗰𝗸𝗲𝗿 𝗲𝗻𝗴𝗶𝗻𝗲<br>
↳ The Docker engine is responsible for running and managing containers. It's composed of the Docker daemon and the Docker CLI that communicates through REST API.

𝗗𝗼𝗰𝗸𝗲𝗿 𝗱𝗮𝗲𝗺𝗼𝗻<br>
↳ The daemon is a persistent background service responsible for managing objects. It does so via listening for API requests. Docker objects include images, containers, networks, and storage volumes.

𝗗𝗼𝗰𝗸𝗲𝗿 𝗿𝗲𝗴𝗶𝘀𝘁𝗿𝘆<br>
↳ Are repositories where Docker images are stored and can be distributed from. Docker registries can be public or private. Docker Hub is the default public registry that Docker is configured with.







