# Ansible Architecture :-
******************************

![![Screenshot 2025-05-14 160503](https://github.com/user-attachments/assets/40cf7543-ce54-4aa1-b27c-bbed09258249)
)

## Components :-
___________________
1️⃣ Contrlo-Node :--   When we install and setup in server it's will be  "ansible contrlo-node" ,
                      it is a back bone of the ansible , we don't need to install anything in target 
                      server or worker node of ansible and each targer server have thair own IP adress .
                      
2️⃣ Inventary-File :-- we keep the target file IP's in this file this inveraty file write in "control-node"

3️⃣ Play-Book's :-- by writting Play-Books we can configure  the infrastracture in our environment .
                    we write Play-Book's in  " YAML " Formate ,
                    when we writr a tomact in paly-books and run it  , then it will go to inventary and check the crete 
                    by automation way in target servers it's will install .
                    
4️⃣ SSH -->  SSH the Cannactin  between Play-Books and target servers


## - Key Characteristics of Ansible Architecture

1. agentless:---> Ansible doesn’t require agents or daemons on managed nodes, reducing overhead and simplifying setup.
2. Push-Based:--> The control node pushes configurations and commands to managed nodes, unlike pull-based systems like Puppet or Chef.
3. Modular:-----> Ansible uses modules to perform tasks, which are executed on managed nodes and return results to the control node.
4. Idempotent:--> Ansible ensures that repeated executions of the same task produce the same result, preventing unintended changes.
5. Inventory-Driven:--> Ansible relies on an inventory file to define the hosts it manages.
6. YAML-Based:--------> Playbooks, which define automation tasks, are written in human-readable YAML

# Asible Set-UP 🥇
***********************
