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
   ```bash
   git clone https://github.com/pandacloud1/DevopsProject2.git
   cd DevopsProject2
   code .   # this command will open VS code in backend
   ```
   




 
