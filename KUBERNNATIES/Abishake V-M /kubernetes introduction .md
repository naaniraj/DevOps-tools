SOURCE :https://www.youtube.com/watch?v=dfxrdoEQe00&list=PLdpzxOOAlwvJdsW6A0jCz_3VaANuFMLpc&index=1
**************************************************************************************************
Kubernetes is very importent .it is the future of devops ,by using kubernetes we can mannge podes and nodes ,
inside pod's we keep the containers ,Containers are efimeral ,it mean short living things ,
Containers die and rewaw any time .

DIFFRENCE BETENN DOCKER AND KUBERNETES 
****************************************
Learn the kubernetes comparing with docker , in genrally 

kubernetes are very davanced concept or tool compare to docker 
1. Resouce utilization
DOCKER
--> it support only single host 
--> when we have 100 servers on top of docker host 
--> if the fisrt container use all the resouces ( cpu and memmory )
--> thare is the many chance lost the last container so automatically
    another all containers aloso  have chance to lost ,
    because the resourcees is not enough to 99 th container
--> it called single host , we don't use in 
KUBERNETES
--> by default kubernetes is a claster .
--> Claster is basically a group of nodes 
--> kubernetes is genrally installed in claster .
--> it is a master and node Archicture 
--> one master node have multiple worker nodes 
  or mutiple master node have mutiple worker nodes 
  so the resources detibute evenly by master node's to worker node's in claster 
--> so we don't get down time on resorce utilizaton .
  
2. Auto Healing
 DOCKER
--> if some one deleted one container
--> the application  running inside the container will be not accessable .
--> in kubernetes if the container deleted , by "auto heliang" optionit can replace,
     but in Docker thare is no option .
--> "Auto Healing" is nothing but if container deleted without manual intervention
    the server started itself .
--> But unfortunetly DOCKER don't have this future .
--> so our container go down
--> so the DevOps engneer con't Monitor continusly .
--> we can't check every time by using docker cammand "docker ps -a".
 KUBERNETES
-->  kubernetes already had replecaset's
-->  we dont need to deply a new container
   EX: if our application receaving 1000 % load on C conatiner's
       in festival sesons the load increse 10,000 %
--> in genrally Kubernetes controll on "YAML" file ,
    we write in YAML file " increse replicaset 1 to 10 (1000 % to 10.000 %)
--> Kubernetes also have one future called H.P.A ( Horizontal Pod AutoScale )
--> we can say when ever the load increse 80 % thrshold of the server spin/create new server
--> like the we can run our application without downtime by using Kuberetes
    --> AUTO-HEALING :
--> the word " Heal " mean's when ever the damage kubernetes has to control the damage .
--> Kubernetes Control and fix the damage .
  EX:- If our container going down ,the kubernetes by using auto healing future
   before server going down it will start new server
  -- HOW IT WORK --
=====================
--> In Kubernetes have a "API-Server"
--> when the the server go down the "API-Server" understand and immediatly it will roll out a new container
--> so the application work somoothly the any issues.
--> but kubernetes deal with Pod's

3.Auto Scaling
 DOCKER
--> the docker don't have "Auto Scaling"
--> if you have one container one one docker host ,if it's have resources (4GB-ram-4CPO)
--> if we have 1000 users in our applicatiom
--> in festival time the users will be increse 10,000 uses
--> as per the load we have th increse the servers but in DOCKER  it don't have this future 
--> if we use docker in our aplication it's go down 
KUBERNETES
--> IN kuber netres by sing AUTO-SCALING we can increse the servers as per our load 
--> in oue resources utilizatin increse up to 80 % we can set spin the new server to scale up the server 
to run our application without downtime .
             

  
