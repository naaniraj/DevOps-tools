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
   
## 1 . Infrastructure Setup Using Terraform

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
 
     
 ## 2 . Configure Sonar-QUBE 🛡️

 in CLI 📟 ....---> vopy the https ptth<br>
 ( access jenkins server here -----> http//100.24.54.83:8080 )<br>
-->🔍 http//100.24.54.83:8080 --> Access the jenkis <br>
    -> 👤 USER: niranjan -> 🔓 PASS-WD : NRraju@143<br>

---> acees Sonar-qube URL same as jenkins <br>
    ( access Sonar-Qube server here -----> http//100.24.54.83:9000 )<br>
   --> 🔍 http//100.24.54.83:9000 --> access Sonar-Qube<br>
   -->user:-admin -->pass w/d :-admin<br>
   -> 👤 USER: admin -> 🔓 PASS-WD : NRraju@143  <br>

   #### WEB-HOOK for Sonar-Qube 🪝

   ---> Sonar-QUBE Web-Page --> Admistration --> Configaration --> Web-hooks
    ==> CREATE --> Name : SonarQube-Webhook
               --> URL  : copy and paste the jenkins URL ( http//100.24.54.83:8080/SonarQube-Webhook ) 
                        *sonarqube name name and url of jenkins of sonarqube         ===>> CREATE
              { it will sending real time notification to  jenkis }

#####  ➕ Create Tocken 🔑
---> Security --> Users --> tocken --> click on the hirizotal line ( Update tockrn )
  -->**Genrate tocken** :- 
    - Name :- Sonar tocken  ===> Genrate [*🔑]( copy that tocken save it some whare )
   --> go to jenkia --> Manage jenkins --> Credentiala --> System -->  Global credentials (unrestricted)

   { we should Create  Sonar-tocken , Access-key , Serect-key }
   
   ==> ➕ Add credentials 
      -> Kind : ^ (secect text)
      -> secect : ********( paste the  [*🔑])
      -> ID  : Sonar-tocken
      -> Decription : Sonar-tocken
                    ===> CREATE 
      { Like this we can add Sonar-Qube Tocken in Jenkis }
      
   [ add few more credentials of access-key like AWS ]
   ==> ➕ Add credentials 
      -> Kind : ^ (secect text)
      -> secect : ******** give access key of AWS ( paste the  [*🔑])
      -> ID  : Access-key
      -> Decription : Access-key
                    ===> CREATE 

   [ add few more credentials of Secect-key like AWS ]
   ==> ➕ Add credentials 
      -> Kind : ^ (secect text)
      -> secect : ******** give Secrect key of AWS ( paste the  [*🔑])
      -> ID  : Serect-key
      -> Decription : Serect-key
                    ===> CREATE 
      { we have to give Sonar-tocken , Access-key , Serect-key }    

 ## 2 .  Configure Jenkins 🤖  - 🔌Plugins

 ---> Manage Jenkis --> Plugins --> Avalable Plugins -->  🔍 serch bar
   --> ✅ - SonarQube Scaner
   --> ☑️ - NodeJS
   --> ✅ - Pipeline :Stage View
   --> ☑️ - Eclipse Temurin installer
   --> ✅ - Docker
   --> ☑️ - Docker Commons 
   --> ✅ - Docker Pipeline
   --> ☑️ - Docker API 
   --> ✅ - Docker -Build -Step
   --> ☑️ - Prometheus metrics 
                  ===> INSTALL 
         --->  ☑️ Restart Jenkins when installation is complete ( the jenkis will restart )

  #### ➕ . Configurw the jenkis system and sonar-qube setup
   ----> Manaje jenkis --> System --> 
      ---> SonarQube Server --> Sonar qube installations  -->
      -> Name : SonarServer
      -> Server URL : http//100.24.54.83:9000 { give the Sonarqube URL }
      -> Server Authenticatin Tocken ^ {select"Sonar-tocken"}
                                     ==> SAVE 

 #### . ➕  Set-up Diffrent TOOL's in Jenkis 
  ----> Manage Jenkis --> Tool's --> 
    ---> JDK installation -->  jDK
    -> Name : jdk
    -> ☑️ Install Automatically 
    -> ^* Add installer {select"Install from adoptium.net"}
    -> ^* jdk-17.0.8.1+1 {select which version jdk you want}
        [ you can multiple versions if we want ]
        
   ---> SonarQube Scanner installations 
     -> Name : SonarQube Scanner 
     -> ☑️ Install Automatically 
     -> Version : SonarQube Scanner 6.2.1.4610

   ---> NodeJS installations
     -> Name : NodeJS
     -> ^* Add installer
     -> ☑️ Install Automatically 
     -> Version : NodeJS 16.20.0

   ---> Docker  installations 
     -> Name : Docker
     -> ☑️ Install Automatically 
     ->  ^* Add installer {select"Download from docker.com"}
     -> Docker version : latest
                       ==> SAVE
    [ like this we can intigrate tools in Jenkis ]

## 3 . Build Pipeline Overview 🔁
 + New-item --> Name : Build-Pipeline --> ^*{select"pipeline"} --> ✅OK
   --> PIPELINE  - 🔁

        pipeline {
         agent any
   
    
    
                   
                                                          
   




      
   




 
