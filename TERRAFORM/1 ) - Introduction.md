### 1 What is terraform ?
*******************************
terraform is an open-source infrastracture as a code (lac) tool created by hashicorp,
terraform allows users to build,change,and version infrastracture safely and effeciently,
it can automate and manage our infrastucture.

Terraform is an open-source Infrastructure as Code (IaC) tool that allows you to define and
provision infrastructure using a declarative configuration language. 
It helps automate the setup of resources across multiple cloud providers and services."

### 2 what is terraform state file ?
******************************************
state file will maintain thr current infrasture information ,
when we deploy the resource which cource we gonna deploy ,its will record of the information of the files.

### 3 Restore statefile 
********************************
if we delete the state file ,we can restore it using terraform import cammand 
EX:- Terraform import <file> <resource ID>

