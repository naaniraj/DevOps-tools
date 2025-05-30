# Docker-Swam
******************
👉 Docker swarm is an orchestration service in <br>
   docker that allows us to manage and handle multiple containers at the same time.<br>	
👉 It is a group of servers that runs the docker application. <br> 
   It is used to manage the containers on multiple servers.<br>
👉 This can be implemented by the cluster.The activities<br>
    of the cluster are controlled by a swarm manager,<br>
👉 and machines that have joined the cluster is called swarm worker.<br>

## Docker-Swam Architecture
*********************************

[![![Screenshot 2025-05-30 172555](https://github.com/user-attachments/assets/95ff7e06-7811-4888-ad22-7f72664bdc5d)
)

 🔸	There are mainly worker nodes and manager nodes.<br>
 🔹	Docker Engine helps to create Docker Swarm.<br>
 🔹	There are mainly worker nodes and manager nodes.<br>
 🔸	The worker nodes are connected to the manager nodes.<br>
 🔹	So any scaling or update needs to be done first it will go to the manager node.<br>
 🔸	From the manager node, all the things will go to the worker node.<br>
 🔹	Manager nodes are used to divide the work among the worker nodes.<br>
 🔸	Each worker node will work on an individual service for better performance.<br>

 ## KEY FEATURES OF DOCKER SWARM:
 
📚**Node Clustering**: <br>
Docker Swarm allows you to create a group of Docker hosts that work together as a cluster.<br>
Each host in the cluster is referred to as a "node."<br>

 📚**Service Deployment**: <br>
 You can define services, which are the applications you want to run, <br>
and deploy them across the Docker Swarm cluster. <br>
Docker Swarm ensures that the services are distributed and run on the available nodes.<br>

📚**Load Balancing**: <br>
Swarm includes built-in load balancing, distributing incoming requests among the various <br>
instances of a service running on different nodes. This helps in scaling applications and<br>
improving performance.

📚**High Availability**: <br>
Docker Swarm provides high availability by <br>
automatically rescheduling tasks (individual units of a service) to healthy nodes in case of node failures.<br>

📚**Scalability**:<br>
You can easily scale your applications by adding or removing nodes from the Swarm cluster. <br>
This allows you to adapt to changes in demand for your services.<br>



