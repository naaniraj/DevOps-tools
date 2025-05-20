# Basic Interview Question
*************************************
1- What is Terraform, and what is its primary purpose?<br>
2-  How does Terraform differ from other IaC tools like CloudFormation or Ansible?<br>
3-  What are the key Terraform commands, and what do they do?<br>
4- What is a Terraform state file?<br>
5- What are Terraform providers, and why are they important?<br>
6 -What are Terraform modules?<br>
7- How does Terraform manage remote state?<br>
8 - What are Terraform workspaces, and when should you use them?<br>
9- How does Terraform handle importing existing infrastructure, and what are the limitations?<br>

10- What are Terraform provisioners, and when should you use them?<br>
11- What is drift detection in Terraform, and how can it be addressed?<br>
12- How would you implement a rolling update using Terraform for an application deployed in multiple instances?<br>

13 - How do you handle resource dependencies in Terraform, and what is the role of implicit and explicit dependencies?<br>

14-  How do you manage complex multi-cloud deployments with Terraform?<br>
15-  What are the taint and untaint commands in Terraform? How would you use them in a real-world scenario?<br>

16- What are zero-downtime deployments, and how can Terraform achieve them?<br>
17- How do you handle secrets management in Terraform, and what are the best practices?<br>

18- Explain the concept of remote state locking in Terraform and its importance in team collaboration.<br>

***********************************************************************************************

# DevOps Interview & Scenario-Based Questions 

1 -tell me about current devops projects and what are your daily roles and responsibilites<br>
2 -how do u identify and resolve the high cpu memory usage linux server<br>
3 -write shell script process to restart if it is not running<br>
4 -can you please explain me situation where you handle git merge conflict during hotfix in a live production branch<br>
5 -how do you enforce branch protection and code reviews in github cicd pipelines<br>
6 -what are strategies you have used to reduce docker image size and speed up build time<br>
7 -how do you handle persistent data in docker real time<br>
8 -how do you argocd fit to gitops workflow of cicd pipeline<br>
9 -how do you configure high availability and application on aws using easy to alb autoscaling<br>
10 -how do you monitor infrastructure setup alerts in downtime<br>
11 -vpc peering one vpc db in singapore another one is mumbai region this two regions how do you communicate<br>
12 -what is the process where you guys maintaining the state file<br>
13 -how do you use terraform provisioning vpc with public and private subnets<br>
14 how do u integrate sonarqube code quality checks and nexus artifactory with jenkins pipeline<br>
15 -how did you handle situation where k8 prod was going to crash loop back off state<br>
16 -what is approach zero downtime deployment in k8<br>

****************************************************************
# Real-Time DevOps Interview Questions 

**🧩 Kubernetes**<br>
➤ Why does a Kubernetes pod remain in the Pending state?<br>
➤ What are PersistentVolume (PV) and PersistentVolumeClaim (PVC) in Kubernetes? Real-time usage?<br>
➤ What is the difference between Liveness and Readiness probes? How to configure them?<br>
➤ What is Horizontal Pod Autoscaler (HPA) in Kubernetes and when do you use it?<br>

**🐳 Docker**<br>
➤ A Docker container is running, but the application is not accessible — what could be the reason?<br>
➤ What’s the difference between CMD and ENTRYPOINT in a Dockerfile? When to use each?<br>
➤ What does the Docker architecture look like in real use cases?<br>
➤ Can you share a real-time Docker Compose file example?<br>

**⚙️ Jenkins & CI/CD**<br>
➤ Write a Jenkins Declarative Pipeline with multiple stages.<br>
➤ How many Jenkins slave agents are there in your project and what is their capacity?<br>

**🧬 Git & Source Control**<br>
➤ What’s the difference between git revert and git reset?<br>
➤ What Git branching strategies do you follow in your team?<br>

**🐚 Shell Scripting**<br>
➤ Write a shell script to archive files older than 7 days.<br>
➤ Extend it to send an alert if disk usage exceeds 80%.<br>

**🏗️ Terraform & IaC**<br>
➤ What are the key lifecycle stages in Terraform?<br>
➤ How do you review infrastructure changes before applying in Terraform?<br>
➤ How is Terraform state locking managed in teams?<br>
➤ Given a CIDR block in AWS, how would you design and subnet a VPC?<br>

**☁️ AWS**<br>
➤ What are the different types of Load Balancers in AWS and when do you use each?<br>

**🐍 Python**<br>
➤ Where have you recently used a Python script in your DevOps project?<br>
➤ What modules did you use and why?<br>

**🧱 Linux & OS Concepts**<br>
➤ What’s the difference between hard and soft links in Linux?<br>
➤ How do you use sed and awk for text processing?<br>
➤ How do you find the Process ID (PID) of a Linux process?<br>

1 .How would you approach a CI/CD pipeline failure?<br>
2 .How do you manage infrastructure as code with tools like Terraform? <br>
3 .How would you handle a Docker container not starting?<br>
4 . How do you implement monitoring and logging for systems?<br>
5 . How would you ensure high availability and disaster recovery?<br>


Interview Questions - Cloud & DevOps Engineer Role.

L1 Questions:

1️⃣ In Git, explain the push and pull commands.<br>
2️⃣ What is the use of Git tags?<br>
3️⃣ What are the different types of branches in Git?<br>
4️⃣ How do you write an Ansible playbook, and what client requirements do you consider?<br>
5️⃣ In Python, what are lists and tuples, and how do they differ?<br>
6️⃣ In CloudWatch, what is the use of log groups and log trails?<br>
7️⃣ In Terraform, what is the purpose of init, plan, and apply commands?<br>
8️⃣ What happens if the Terraform state file is accidentally deleted?<br>
9️⃣ What is the purpose of creating S3 bucket policies?<br>
🔟 How do you maintain the lifecycle of an S3 bucket?<br>
1️⃣1️⃣ In Airflow, if a job fails, how do you debug it?<br>
1️⃣2️⃣ If you're facing performance issues on a server, how do you troubleshoot?<br>

 L2 Questions:

1️⃣ What are Network ACLs and Security Groups, and how do they differ?<br>
2️⃣ Explain EC2 instances and handling multiple VPCs.<br>
3️⃣ How do you configure AWS RDS, and what factors do you consider (size, requirements, etc.)?<br>
4️⃣ How much data is stored in your RDS MySQL?<br>
5️⃣ How many masters and slaves are in RDS?<br>
6️⃣ How do you configure a Grafana dashboard?<br>
7️⃣ What kind of CI/CD pipelines are you familiar with?<br>
8️⃣ Explain Declarative vs. Scripting pipelines.<br>
9️⃣ In Kubernetes, if a pod is in a pending state, how do you troubleshoot?<br>
🔟 If Docker containers are consuming too much disk space, how do you fix it?<br>
1️⃣1️⃣ In Linux, how do you attach and detach a filesystem?<br>
1️⃣2️⃣ How do you print the last 15 lines of a file in Linux?<br>
1️⃣3️⃣ How do you enable passwordless authentication between two servers?<br>



******Interview Question For Fresher******<br>
1.What is DevOps Lifecycle?<br>
2.Have you used any Linux Flavors, if yes, which one?<br>
3.What is the command to change the ownership and permission of a file or directory in Linux?<br>
4.How do you manage and view running processes in Linux?<br>
5.What is SSH?<br>
6.What is DNS (Domain Name System), and how does it work?<br>
7.What is NAT(Network Address Translatioj), and why is it used?<br>
8.Explain the difference between TCP and UDP Protocols.<br>
9.What os Git and how do we use it in DevOps?<br>
10.Explain the workflow of how to push the code from a local machine.<br>
11.How do you revert a commit that you made in your repository?<br>
What is a Branch in a Repository?<br>
13.What cloud you are familiar with?<br>
14.What is VPC in cloud?<br>
15.What is the difference between a Private and Public Subnet and what differentiates it?<br>
16.What is the Deifference between reserved instance and spot instances?<br>
17.What is CloudFormation (AWS) ?<br>
18.What are the popular IaC tools have you used?<br>
19.What is the difference between Terraform & Ansible?<br>
20.What is a playbook in Ansible?<br>

### Senario Based Questions
*******************************
1.Suppose the particular stage is failed.immediately inform to concerned team How to do?<br>
2.Suddenly all jenkins jobs are deleted accidentally How to restore it?<br>
3.Can you explain parallel builds in jenkins?<br>
4.Do you have any idea about Image pull secrets?<br>
5.what is the difference between public subnet and private subnet?<br>
6.Which type of load balancer is fast like application or network load balancer?<br>
7.in PUBG game which type of aws load balancer we can use?<br>
8.How you can maintain keys passwords in terraform configuration file?<br>
9.In terraform where you need to change existing infrastructure and so how you do execute and plan to minimise downtime of an infrastructure<br>
10.If you have three tier architecture in aws and how you can secure your application?<br>



  

   

   

   
