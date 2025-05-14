## Ansible Architecture :-
******************************

![![ansible-ar](https://github.com/user-attachments/assets/31df5bd2-d00a-4ec9-9bd3-b4e5be8da831)
)

## Components :-
___________________

when we run configure the ansible its will crete lr install the software and our requrement softwares 
in the node servers as per our palybook

## - Key Characteristics of Ansible Architecture

1. agentless:---> Ansible doesn’t require agents or daemons on managed nodes, reducing overhead and simplifying setup.
2. Push-Based:--> The control node pushes configurations and commands to managed nodes, unlike pull-based systems like Puppet or Chef.
3. Modular:-----> Ansible uses modules to perform tasks, which are executed on managed nodes and return results to the control node.
4. Idempotent:--> Ansible ensures that repeated executions of the same task produce the same result, preventing unintended changes.
5. Inventory-Driven:--> Ansible relies on an inventory file to define the hosts it manages.
6. YAML-Based:--------> Playbooks, which define automation tasks, are written in human-readable YAML
