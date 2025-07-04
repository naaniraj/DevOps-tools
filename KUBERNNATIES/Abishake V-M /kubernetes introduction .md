SOURCE :https://www.youtube.com/watch?v=dfxrdoEQe00&list=PLdpzxOOAlwvJdsW6A0jCz_3VaANuFMLpc&index=1
**************************************************************************************************
Kubernetes is very importent .it is the future of devops ,by using kubernetes we can mannge podes and nodes ,<br>
inside pod's we keep the containers ,Containers are efimeral ,it mean short living things ,<br>
Containers die and rewaw any time .<br>

DIFFRENCE BETENN DOCKER AND KUBERNETES 
****************************************
Learn the kubernetes comparing with docker , in genrally <br>
kubernetes are very davanced concept or tool compare to docker <br>
1. Resouce utilization<br>
DOCKER<br>
--> it support only single host <br>
--> when we have 100 servers on top of docker host <br>
--> if the fisrt container use all the resouces ( cpu and memmory )<br>
--> thare is the many chance lost the last container so automatically<br>
    another all containers aloso  have chance to lost ,<br>
    because the resourcees is not enough to 99 th container<br>
--> it called single host , we don't use in <br>
KUBERNETES<br>
--> by default kubernetes is a claster .<br>
--> Claster is basically a group of nodes <br>
--> kubernetes is genrally installed in claster .<br>
--> it is a master and node Archicture <br>
--> one master node have multiple worker nodes <br>
  or mutiple master node have mutiple worker nodes <br>
  so the resources detibute evenly by master node's to worker node's in claster <br>
--> so we don't get down time on resorce utilizaton .<br>
  
2. Auto Healing<br>
 DOCKER<br>
--> if some one deleted one container<br>
--> the application  running inside the container will be not accessable .<br>
--> in kubernetes if the container deleted , by "auto heliang" optionit can replace,<br>
     but in Docker thare is no option .<br>
--> "Auto Healing" is nothing but if container deleted without manual intervention<br>
    the server started itself .<br>
--> But unfortunetly DOCKER don't have this future .<br>
--> so our container go down<br>
--> so the DevOps engneer con't Monitor continusly .<br>
--> we can't check every time by using docker cammand "docker ps -a".<br>
 KUBERNETES<br>
-->  kubernetes already had replecaset's<br>
-->  we dont need to deply a new container
   EX: if our application receaving 1000 % load on C conatiner's<br>
       in festival sesons the load increse 10,000 %<br>
--> in genrally Kubernetes controll on "YAML" file ,<br>
    we write in YAML file " increse replicaset 1 to 10 (1000 % to 10.000 %)<br>
--> Kubernetes also have one future called H.P.A ( Horizontal Pod AutoScale )<br>
--> we can say when ever the load increse 80 % thrshold of the server spin/create new server<br>
--> like the we can run our application without downtime by using Kuberetes<br>
    --> AUTO-HEALING :<br>
--> the word " Heal " mean's when ever the damage kubernetes has to control the damage .<br>
--> Kubernetes Control and fix the damage .<br>
  EX:- If our container going down ,the kubernetes by using auto healing future<br>
   before server going down it will start new server<br>
  -- HOW IT WORK --<br>
=====================
--> In Kubernetes have a "API-Server"<br>
--> when the the server go down the "API-Server" understand and immediatly it will roll out a new container<br>
--> so the application work somoothly the any issues.<br>
--> but kubernetes deal with Pod's<br>

3.Auto Scaling<br>
 DOCKER<br>
--> the docker don't have "Auto Scaling"<br>
--> if you have one container one one docker host ,if it's have resources (4GB-ram-4CPO)<br>
--> if we have 1000 users in our applicatiom<br>
--> in festival time the users will be increse 10,000 uses<br>
--> as per the load we have th increse the servers but in DOCKER  it don't have this future<br> 
--> if we use docker in our aplication it's go down <br>
KUBERNETES<br>
--> IN kuber netres by sing AUTO-SCALING we can increse the servers as per our load <br>
--> in oue resources utilizatin increse up to 80 % we can set spin the new server to scale up the server <br>
to run our application without downtime .<br>
             

  
