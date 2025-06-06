## How to Wrire Pipeline 🔁-🔁-🔁
***********************************-

After Configaration of Plugins And tools  use hallo-word syntx to write better
and copy and peaste multiple times for mutiple stages 

### Buld Pipeline
1 . this is 1 st stage intigrate pipeline with git repo
___________________________________________________

    pipeline {
        agent any

        tools {
          jdk 'JDK'
          NodeJS 'NodeJS'
        }

        parameters {
            string (name: 'ECR_REPO_NAME', defalutvalue: 'amazon-prime' ,decription: 'enter your repositery name')
        }
         

        environment {
            SCANER_HOME = tool 'SonarQube Scaner'
        }
        
        
        stages {
            stage ('git checkout') {
                steps {
                    git branch : 'main',
                    url : ( ** copy and peaste the our source code repo by pipeline syntax under folling steps ** )
                               
--> go to pipeline syntax --> Sample step { select *^ "git:Git" }<br>
--> Repository URL: " your github url --> Branch : main/Master
--> Credentials : select Your credentilas 
    ---> GENRATE PIPELINE SCRIPT 
    ( copy and peaste in git checkout step )

--> IN tools we have to mention which tool we difine in jenkins 
--> 

2 . this is 2 nd stage to intigrate with SonarQube 
______________________________________________________

          stage ('sonar-qube analysis') {
              steps {
                  WithSonarQubeEnv : ( 'Sonar-Server')
                     $SCANER_HOME/bin/SonarQube Scaner \
                     -Dsonar.projectName=amazon-prime \
                     -Dsonar.projectkey=amazon-prime
                  

--> go to pipeline syntax --> Sample step { select *^ "WithSonarQubeENV:" }
     ---> GENRATE PIPELINE SCRIPT 
        ( copy and peaste in SonarQube analysis step )

 3 . this is 3 rd stage to check the qulity gate 
 _____________________________________________________
       
          stage ('SonarQube Qulity Gate') {
              steps {
                  (**path of SonarQube Quality Gate path by pipeline syntax**)

---> go to pipeline syntax --> Sample step {select *^ "WaitForQulityGates"}
  --> Server Authentication tocken {select *^ "Sonar-Tocken"}
       ---> GENRATE PIPELINE SCRIPT 
        ( copy and peaste in SonarQube Qulity Gate step )   

 4 . NPM install 
 _________________

         stage ( 'NPM install') {
             steps {
                 sh "npm install"

--> it's simple cammand to install NPM              
                 
5 . we intigrate Trivy  for check vernarabulitys in the code with pipeline
______________________________________________________________________________
        
          stage ( 'Trivy Scan') {
             steps {
                 sh "Trivy fs . > trivy-scan-results.txt"

--> we use trivy for is theare any vernarabulitys to secure the application 
--> "trivy-scan-results.txt" we store the result in this file
--> the text file give the result about vernarabulitys

6 . Docker to build Docker Image 
_______________________________________

     stage ('Docker image build') {
         steps {
             sh "docker build -t ${params.ECR_REPO_NAME} ." 

---> add parameters in the first lines of pipeline   

7 . this stage for create ECR repository
__________________________________________

    stage ('creatr ECR repo') {
        steps {
            ( ** copy and peaste the our source code repo by pipeline syntax under folling steps ** )
            sh """
            aws configure set aws_access_key_id $AWS_ACCESS_KEY
            aws configure set aws_secrect_key_id $AWS_SCRECT_KEY
            aws ecr create-repository --repository-name ${params.ECR_REPO_NAME} --region us-east-1
            aws ecr describe-repository --repository-name ${params.ECR_REPO_NAME} --region us-east-1
            """

            
--> go to pipeline syntax --> Sample step {select *^ "WithCredentials: Bind Credentila with variables"} 
 --> Binding : {select *^ "Screct Text"} --> Variable : AWS_ACCESS_KEY 
 --> Credentials : Access-key --> ^add : {select *^ "Screct Text"}
  --> Variable:AWS_SCRECT_KEY  Credentials : *^ serect-key 
                 ====> GENRATE PIPELINE SCRIPT
 --> in the 2 and 3 line configare the aws key and call the variable "$AWS_ACCESS_KEY"  & "$AWS_SCRECT_KEY"  
  ( like this we can give access key and screct key withot exposing )
  
8 ' Login to ECR 
_____________________

     stage ('login to ECR & tag image' ) {
        steps {
           (** copy the systax path of 7th stage 1 line and keep here**)
           ( run the cammands as per our accounnt credentials like a account ID
           by calling parameeters  )
           


---> go to aws account -->  ECR( Elastic Container Registry) --> Create a repository 
 --> create --> Rep"" Name : test      =====> Create 
 --> test --> view push cammands ( it will show you how to login to ECR and how to build image ,
                                how to tag and how to push the image 
NOTE : you can find this pipeline vedeo in youtube at 1:27 time 
  YOUTUBE : https://www.youtube.com/watch?v=Gd9Aofx-iLI&t=4239s

  9 . push the image to AWS ECR 
  _______________________________
  
     stage ('push the image to aws ECR') {
         steps {
            ( ** keep the first line of the 8 th stage** )
            and paste the push cammand and insted of id image give parameter 


 10 . Clean up the images from jenkisn serer 
 _______________________________________________
  when we buld image multiple times the privius images will accupay some space
  by using this stage we can remove old images and keep latest build images in jenkins

         stage ('Clean up the images from jenkins') {
             steps {
                (*write the 2 cammands of the 9 th stage and just rmi in the cammand
                 for remove the old images )


                 


### Running Jenkins Pipeline 
*******************************
Create and run the build pipeline in Jenkins. The pipeline will build, analyze, and push the project Docker image to ECR.
Create a Jenkins pipeline by adding the following script:
---> finally the pipeline look like this 
### Build Pipeline

```groovy
pipeline {
    agent any
    
    parameters {
        string(name: 'ECR_REPO_NAME', defaultValue: 'amazon-prime', description: 'Enter repository name')
        string(name: 'AWS_ACCOUNT_ID', defaultValue: '123456789012', description: 'Enter AWS Account ID') // Added missing quote
    }
    
    tools {
        jdk 'JDK'
        nodejs 'NodeJS'
    }
    
    environment {
        SCANNER_HOME = tool 'SonarQube Scanner'
    }
    
    stages {
        stage('1. Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/pandacloud1/DevopsProject2.git'
            }
        }
        
        stage('2. SonarQube Analysis') {
            steps {
                withSonarQubeEnv ('sonar-server') {
                    sh """
                    $SCANNER_HOME/bin/sonar-scanner \
                    -Dsonar.projectName=amazon-prime \
                    -Dsonar.projectKey=amazon-prime
                    """
                }
            }
        }
        
        stage('3. Quality Gate') {
            steps {
                waitForQualityGate abortPipeline: false, 
                credentialsId: 'sonar-token'
            }
        }
        
        stage('4. Install npm') {
            steps {
                sh "npm install"
            }
        }
        
        stage('5. Trivy Scan') {
            steps {
                sh "trivy fs . > trivy.txt"
            }
        }
        
        stage('6. Build Docker Image') {
            steps {
                sh "docker build -t ${params.ECR_REPO_NAME} ."
            }
        }
        
        stage('7. Create ECR repo') {
            steps {
                withCredentials([string(credentialsId: 'access-key', variable: 'AWS_ACCESS_KEY'), 
                                 string(credentialsId: 'secret-key', variable: 'AWS_SECRET_KEY')]) {
                    sh """
                    aws configure set aws_access_key_id $AWS_ACCESS_KEY
                    aws configure set aws_secret_access_key $AWS_SECRET_KEY
                    aws ecr describe-repositories --repository-names ${params.ECR_REPO_NAME} --region us-east-1 || \
                    aws ecr create-repository --repository-name ${params.ECR_REPO_NAME} --region us-east-1
                    """
                }
            }
        }
        
        stage('8. Login to ECR & tag image') {
            steps {
                withCredentials([string(credentialsId: 'access-key', variable: 'AWS_ACCESS_KEY'), 
                                 string(credentialsId: 'secret-key', variable: 'AWS_SECRET_KEY')]) {
                    sh """
                    aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin ${params.AWS_ACCOUNT_ID}.dkr.ecr.us-east-1.amazonaws.com
                    docker tag ${params.ECR_REPO_NAME} ${params.AWS_ACCOUNT_ID}.dkr.ecr.us-east-1.amazonaws.com/${params.ECR_REPO_NAME}:${BUILD_NUMBER}
                    docker tag ${params.ECR_REPO_NAME} ${params.AWS_ACCOUNT_ID}.dkr.ecr.us-east-1.amazonaws.com/${params.ECR_REPO_NAME}:latest
                    """
                }
            }
        }
        
        stage('9. Push image to ECR') {
            steps {
                withCredentials([string(credentialsId: 'access-key', variable: 'AWS_ACCESS_KEY'), 
                                 string(credentialsId: 'secret-key', variable: 'AWS_SECRET_KEY')]) {
                    sh """
                    docker push ${params.AWS_ACCOUNT_ID}.dkr.ecr.us-east-1.amazonaws.com/${params.ECR_REPO_NAME}:${BUILD_NUMBER}
                    docker push ${params.AWS_ACCOUNT_ID}.dkr.ecr.us-east-1.amazonaws.com/${params.ECR_REPO_NAME}:latest
                    """
                }
            }
        }
        
        stage('10. Cleanup Images') {
            steps {
                sh """
                docker rmi ${params.AWS_ACCOUNT_ID}.dkr.ecr.us-east-1.amazonaws.com/${params.ECR_REPO_NAME}:${BUILD_NUMBER}
                docker rmi ${params.AWS_ACCOUNT_ID}.dkr.ecr.us-east-1.amazonaws.com/${params.ECR_REPO_NAME}:latest
		docker images
                """
            }
        }
    }
}
 
            

        
                  
              
    
   
 
               


            
