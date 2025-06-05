# Kubernetes Architecture 

![Screenshot 2025-04-10 110501](https://github.com/user-attachments/assets/1885b936-8f3a-4899-b91f-83fa659304d3)
)

**PODE'S** : pode 's are small deployable units in the kubernetes claster ,pod can hold one or more containers <br>
**NODE'S** : A pod can have single or multiple podes inside of it ,<br>

##  Kubernetes Components : -

### control panel :-

1️⃣***APIServer*** :-<br>
its frent-end of our Kubernetes master claster , it will comuunicate with all other components ,<br>
it will authenticate the user and validate our requests ,if we wnat to create a pod by this component we can create ,<br>
it retrive the data ( if we want get some data we cn get by this component) , and update the claster information in " ETCD " component ,<br>
also it will talk with  or instruct " KUB-LET" that run on worker node to create a node's and pod's ,<br>
its reseave the request from user or application , and check the requests ia valed or not ,and communicate with clasters .<br>

2️⃣***schedular***  :- <br>
when the pod is created  the schedular check is there any helthy nods or not and select the best node and alocate or givethe load to the pod ,<br>


3️⃣***Controller*** :- its a manager of the pods ,if the pod is fail or running down  ,it's will create or replace new pod to keep running smoothly our application
     
4️⃣ ***etcd***       :- it's store and maintain the date about the claster and nodes information .
                       

 ### Worker Node 's  :-  

1️⃣***kube-proxy*** :- it's maintain the network communication betwwn nodes and pods ,handles the route traffic , destribute the load evenly to the pods to running application smoothly ,for pod to pod communication
  
2️⃣***kubelet***    :-  it's a care taker of the pods in each nodes , check the helth of the nodes and  rport to the contrl plane  to run efeciently .



