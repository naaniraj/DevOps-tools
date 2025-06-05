## 1) What is Kubernetes? / What do you understand by Kubernetes?<br>
Kubernetes is an open-source container-orchestration tool or system used to automate tasks such as the<br>
management, monitoring, scaling, and deploying containerized applications.<br>
________________________________________
## 2) What is the use of Kubernetes?<br>
Kubernetes is mainly used to easily manage several containers (since it can handle the grouping of containers),<br>
which provides logical units that can be discovered and managed.<br>
________________________________________
## 3) Who was the inventor of Kubernetes?<br>
Kubernetes was initially designed and developed by Google and is now maintained by the Cloud Native Computing Foundation.<br>
____________________________________________________________________________________________
## 4) What are K8s?<br>
K8s is nothing but just another term for Kubernetes.<br>
________________________________________
## 5) What was the main motive behind the development of Kubernetes?<br>
The main motive behind the development of Kubernetes is to provide a "platform for automating deployment,<br>
scaling, and operations of application containers across clusters of hosts."<br>
________________________________________
## 6) What do you understand by the term orchestration when it comes to software and DevOps?<br>
The term orchestration specifies integrating multiple services that allow them to automate processes<br>
or synchronize information in a specific time sequence.<br>
For example, suppose we have six or seven microservices for an application to run,<br>
then if you place them in separate containers, this would inevitably create obstacles for communication. Using orchestration,<br>
we can do it quickly to enable all services in individual containers to work seamlessly to accomplish a single goal.<br>
________________________________________
## 7) What is the relation between Docker and Kubernetes?<br>
Docker is an open-source platform used to handle software development.<br>
It is mainly used to package the settings and dependencies that the software/application needs to run into a container,<br>
which allows for portability and several other advantages. On the other hand,<br>
Kubernetes is used to allow the manual linking and orchestration of several containers,<br>
running on multiple hosts that have been created using Docker.<br>
________________________________________
## 8) What are the key differences between the Docker Swarm and Kubernetes?<br>
Docker Swarm is an open-source container orchestration platform used to cluster and schedule Docker containers. <br>
It is a native of Docker. Following is the list of key differences between the Docker Swarm and Kubernetes<br>

**Docker Swarm** 🐳<br>
1️⃣-is easy and convenient to set up, but it doesn't have a robust cluster.<br>
2️⃣-Docker Swarm can't do auto-scaling as the Kubernetes can do, but Docker's scaling is five times faster than Kubernetes.	<br>
3️⃣ Docker Swarm doesn't provide a GUI.<br>
4️⃣ Docker Swarm provides an automatic load balancing feature of traffic between containers in a cluster.<br>
5️⃣ Docker requires third-party tools such as the ELK stack for logging and monitoring<br>
6️⃣ In Docker Swarm, we can easily share storage volumes with any container.<br>
7️⃣ We can deploy rolling updates in Docker Swarm but can't deploy automatic rollbacks<br>

**Kubernetes** ☸️<br>
1️⃣-is more complicated than Docker Swarm to set up, but it assures a robust cluster.<br>
2️⃣-Kubernetes can do auto-scaling, but scaling is slower than Docker Swarm.<br>
3️⃣ Kubernetes provides a GUI in the form of a dashboard.<br>
4️⃣ It requires manual intervention in Kubernetes for load balancing such traffic.<br>
5️⃣ Kubernetes provides such integrated tools for logging and monitoring purposes.<br>
6️⃣ In Kubernetes, we can only share storage volumes with containers in the same pod.<br>
7️⃣ In Kubernetes, we can deploy rolling updates as well as automatic rollbacks.<br>
________________________________________
## 9) What do you understand by a node in Kubernetes?<br>
In Kubernetes, a node is the smallest unit of hardware. It is used to define a single machine in a cluster <br>
that can act as a virtual machine from a cloud provider or physical machine in the data center. <br>
Every machine of the Kubernetes cluster can act as a substitute for other machines.<br>
________________________________________
## 10) What is the use of a Kubernetes Kube-scheduler?<br>
A Kube-scheduler is the default scheduler for Kubernetes. It is used to assign nodes to newly created pods.<br>
_____________________________________________________________________
## 11) What do you understand by daemon sets in Kubernetes?<br>
Daemon sets are sets of pods that run on a host and are used for host layers attributes like monitoring network or simple network.<br>
________________________________________
## 12) What is Heapster in Kubernetes?<br>
A Heapster is a metrics collection and performance monitoring system for data collected by the Kublet.<br>
________________________________________
## 13) What are the main reasons behind using Kubernetes?<br>
Kubernetes is mainly used because of the following reasons:<br>
1️⃣ 	We can use Kubernetes easily on on-premises bare metal, OpenStack, public clouds Google, Azure, AWS, etc.<br>
2️⃣ 	Using Kubernetes, we can avoid vendor lock issues as it can use any vendor-specific APIs or<br>
    services except where Kubernetes provides an abstraction , e.g., load balancer and storage.<br>
3️⃣ 	It enables applications that need to be released and updated without any downtime.<br>
________________________________________
## 14) What does the node status contain in Kubernetes?<br>
In Kubernetes, the main components of a node status are Address, Condition, Capacity, and Info.<br>
________________________________________
## 15) What is the Kubernetes Network Policy?<br>
In Kubernetes, the Network Policy specifies how the same namespace's pods would communicate with each other and the network endpoint.<br>
________________________________________

