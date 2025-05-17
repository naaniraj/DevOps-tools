# AWS DevOps CI-CD Project - 2 [Amazon Prime Clone (Fully automated)]
************************************************************************
![![![Screenshot 2025-05-17 080410](https://github.com/user-attachments/assets/b54d2bb1-9ca0-4d99-8da5-e17f0b28ca4e)
)
)

**source**.-.-.--> https://www.youtube.com/watch?v=Gd9Aofx-iLI&t=36s
 
 --> go to the google --> 🔍 [nikhil manglik github]--> clone the reop to your github 🐱 🗂️ Prime-vedeo-clone] -->  

## Configuration
### AWS Setup
1. **IAM User**: Create an IAM user and generate the access and secret keys to configure your machine with AWS.<br>
     ---> go to aws A/C --> 🔍 [ IAM ] --> users --> create user --> user-Name:-{ DevOps-project-User}<br>
        -->  ✅  next <br>
   ---> **Set Permission**
       --> ✅ Attach policy directly <br>
   
   ---->**permissions policy** 🔐<br>
      -> ✅ -Administrater access<br>
      -> ✅ - ( you can select whcich one you want )<br>
       ====> NEXT    =====> Create User<br>

   ---> go to our user { DevOps-project-User } --> Security Credentiol --> Create Access Key<br>
       --> ✅ CLI -Cammand Line Interface -->✅ confermation<br>
                                     ===> NEXT<br>
   
   -->Decription value :- {AWS-Access-Key-Secrect-key}<br>
                                    ===> CREATE ACCESS KEY<br>
   
   [ Copy Those Keys save it some whare ] <br>
                                   ===> DONE <br>
   
   --> 🔍 [ EC2 ] --> key pair --> creatr a key-pair --> <br>
      -->  Name :- Key   --> ✅ RSA --> ✅ .PEM --> <br>
                                   ===> CREATE KEY-PAIR<br>
   [ the key will download in our local machine 📁-->📄 ] <br>
   
## Infrastructure Setup Using Terraform

1. **Clone the Repository** (Open Command Prompt & run below):
   ---> go to git hub copy the code --> before create a folder in local 📁{DevOps-project-2}
    --> open git bah from 📁 --> clone to the code to gitbash
   -$ cd DevOps-Project-2 
   -$ devops project2>code . { it will open VS-Code}
     { you can see all the files in VS-CODE }

   🔤-VS-CODE  ==> terraform_code --> main.tf
   { you can see which infra we gonna create for our project }

   --> copy your .pem file key --> go back to terraform code --> paste at main.tf file
   --> click right key in laptop on main.tf --> open in intigrated terminal -->
   --> Run the below commands to reduce the path displayed in VS Code terminal (Optional)
     ```bash
     code $PROFILE
     function prompt {"$PWD > "}
     function prompt {$(Get-Location -Leaf) + " > "}
     ```
     - Run the following commands:
     ```bash
     aws configure
 { NOW you laptop configured with AWS account and provide access key and screat key }
 
     terraform init
  {this cammand will intlize your repository
  and it will show " Terraform has benn successfully Initializd }

     terrafrom plan
  { it will show which infrastracture we gonna create }
  
     terraform apply --auto-approve
  {it will create the infra ,at the end it's show "Apply complete! resouces: 2 added, 0 changed, 0 destroyed.  
     ```
    
         
   
   
   




      
   




 
