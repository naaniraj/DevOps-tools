## install terraform
[ source: devops and cloud with shiva 76s - day25- terraform ]

--> go to GOOGLE --> 🔍'Terraform Donload' --> windows --> AMD:64 {downlad}
--> 💻 go to 📁 file system in our laptop -->
Extract the file --> you will get exe.file 📄 " create a file and keep the softeare dile like this in the name 'SOFTWARE's 📄 "
 
-- >💻 go to windows 🔍 search " edit the system environment variable "  --> Environment variable 
--> system variable --> 
Edit --> give the path of the our terraform EXE.FILE📄[ -->NEW -->C:\SOFTWARES'S --> OK--> OK --> OK
      ( system will check all the paths whare is in the terraform )
          
      terraform version
      
 " if the terraform is thare it will show the  version of TERRAFORM "
 ## Terraform CLI install
 *************************
 --> go to GOOGLE --> 🔍'AWS cli install ' -->  windows -->
 click the download of the path 
 -->AWS CAMMAND LINE INTERFACE v2 setup 💻 [🌩️ AWS]
   --> next --> next --> install📥--> 
   
        aws --version
" to check the version of aws "

![image](![Screenshot 2025-04-15 105011](https://github.com/user-attachments/assets/f53811c1-c51e-46f8-a8d0-f2e6234c24a8)
)

## WRITE TERRAFORM FILE WITH VS-CODE

-->🐙[Create a Repository in github "Terraform"] -->copy the repo SSH path 
    🐙💻 --> go to git bash 

    cd terraform
    git init
    git branch -m main
    git remote origin (git@github.com:naaniraj/DevOps-tools.git)

--> go to   "VS-CODE"  -->📁[Create a folder "Terraform"]
    ---> 📄Session-1 { you can write terraform code here }

## Installation :

### Ubuntu:

#!/bin/bash

apt update -y <br>
sudo apt install curl wget apt-transport-https -y<br>
sudo curl -fsSL https://get.docker.com -o get-docker.sh<br>
sudo sh get-docker.sh<br>
sudo curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64<br>
sudo mv minikube-linux-amd64 /usr/local/bin/minikube<br>
sudo chmod +x /usr/local/bin/minikube <br>
sudo minikube version<br>
sudo curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"<br>
sudo curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"<br>
sudo echo "$(cat kubectl.sha256) kubectl" | sha256sum --check <br>
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl<br>
sudo kubectl version --client<br>
sudo kubectl version --client --output=yaml   <br>
sudo minikube start --driver=docker --force<br>





### RedHat: 

yum install docker -y<br>
systemctl start docker<br>
systemctl status docker<br>
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"<br>
sudo mv kubectl /usr/local/bin/kubectl<br>
sudo chmod +x /usr/local/bin/kubectl<br>
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64<br>
sudo install minikube-linux-amd64 /usr/local/bin/minikube<br>
sudo yum install iptables -y<br>
yum install conntrack -y <br>
minikube start --driver=docker --force<br>
minikube status <br>

    

  

   

   

   
