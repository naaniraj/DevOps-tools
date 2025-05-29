# Docker - Networking 
*************************
We use docker networks for containers communicate each container .<br>
becouse inside the server containers are fully isolated .<br>
with the help of networks we can  access and control with containers from outside .<br>
in real time one container shoud talk another container .<br>
each conatiner have own uniqe port number to cannact each conatiner and with host.<br>

### ***Different TYPE 'S of Network's*** 

1️⃣-Bridge Network
2️⃣-Host Networking 
3️⃣-Overly Networking ( K8S )

--> each containers dhould communicate each container <br>
EX : login container ,frent-end container .<br>
--> each containers shold talk but if any contaer have sensitive information<br>
   we should restrict to cannact <br>
 EX: Database ,back-end, for sequre sensitive infromation.<br>

 ### ***How a container talk with host operating system*** :
 ⚙️ CONTAINER-1  talk to COTAINER-2
 ⚙️ CONTAINER-1 is isolated with CONTAINER-2

 -> if we have our host server inside we have a container with port number 
    each one communicate it's called bride network 
--> if docker network and host network is same 
   both can talk easyly   

   ## In Practice 
____________________

--> go to cli --> run Nginix image container (login is cont" name )
         
    docker run -d --name login nginix:latest
--> login to the container by using under cammand 

    docker exec -it login  bin/bash
    apt update #basic update
    apt-get install iputils-ping -y #install ping cammand 
    ping -v # to see the ping version

--> run another container called (logout)

    docker run -d --name logout nginix:latest
-->  login to the container by using under cammand     

     docker ps 
     docker inspect login   #you can see the ip adress of login
     ping <ip number>
     docker networks ls      #too see the all the  networks
     docker network rm <networkname>



    
