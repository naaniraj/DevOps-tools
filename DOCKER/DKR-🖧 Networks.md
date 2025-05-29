**SOURCE** : https://www.youtube.com/watch?v=xrUGEoUpa3s&t=1753s
# Docker - Networking 
*************************
We use docker networks for containers communicate each container .<br>
becouse inside the server containers are fully isolated .<br>
with the help of networks we can  access and control with containers from outside .<br>
in real time one container shoud talk another container .<br>
each conatiner have own uniqe port number to cannact each conatiner and with host.<br>
its very crusheal in micro services archtechre .<br>
we can costamize our network as per our usecase .<br>
Docker networking is primarily used to establish communication<br>
between Docker containers and the outside world. Docker supports different types of networks<br>

### ***Different TYPE 'S of Network's*** 

1️⃣-Bridge Network <br>
2️⃣-Host Networking <br>
3️⃣-Overly Networking ( K8S )<br>

### 1️⃣-Bridge Network 🌉
in docker bride network  econtainers caommunicate with each others in  host system  ,<br>
it's a default network mode in docker that let container communicate with vertuval networks ,<br>
It is a private internal network created by Docker on the host .<br>
Eah container connecting to this network get their own internal private network address. <br>
Generally IPS get assigned in the range of 172.17.x.x to the containers.<br>
The containers can access each other using the internal IP. <br>
If we want to access any of these containers from the outside world,<br>
then we need to map the ports of these containers to ports on the Docker host.<br>
The another name of Bridge network is dockerO as it's the default one.<br>

### 2️⃣-Host Networking 🧑‍💼
If we want to access the containers externally, then we can attach the container to Host network ,
There is no network isolation between the host and the container. 

### 3️⃣-Overly Networking 🌐( K8S )


--> each containers dhould communicate each container <br>
EX : login container ,frent-end container .<br>
--> each containers shold talk but if any contaer have sensitive information<br>
   we should restrict to cannact <br>
 EX: Database ,back-end, for sequre sensitive infromation.<br>

 ### ***How a container talk with host operating system*** :
 ⚙️ CONTAINER-1  talk to COTAINER-2<br>
 ⚙️ CONTAINER-1 is isolated with CONTAINER-2<br>

 -> if we have our host server inside we have a container with port number<br>
    each one communicate it's called bride network <br>
--> if docker network and host network is same <br>
   both can talk easyly   <br>

   ## In Practice 
____________________

--> go to cli --> run Nginix image container (login is cont" name )<br>
         
    docker run -d --name login nginix:latest
--> login to the container by using under cammand <br>

    docker exec -it login  bin/bash
    apt update #basic update
    apt-get install iputils-ping -y #install ping cammand 
    ping -v # to see the ping version

--> run another container called (logout)<br>

    docker run -d --name logout nginix:latest
-->  login to the container by using under cammand <br>    

     docker ps 
     docker inspect login          #you can see the ip adress of login
     ping <ip number>
     docker networks ls            #too see the all the  networks
     docker network rm <networkname>
     docker network create secure-network        #the costam network will create in network bridge
     docker networks ls                          #you can see the newly created network & we shoud keep it in secure
     docker run -d --name finance --network=secure-network  nginx:latest
     docker ps         #you can see ( login,logout,finance ) container names
     docker inspect <name od the container>    # its will show "secure-network"
     docker inspect run logout       #its show the netwrk is "bridge"
     pinf <finace contaner ip>       #it wont give any information /its mean we secured the finance container .
     


    
