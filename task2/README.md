# Task2:


## About:

This folder contains:

1. vagrant file: 
    - to create VMs that will be used in the kubernetes claster.
2. kubernetes-setup directory: 
    - that contains ansible playbooks and roles which will configure the nodes and install the needed independencies.
3. deployments directory:
    - includes deployment file to deploy a pod contains all containers and service file to expose the app to the outside.



## Steps 

Provisioning the infrastructure may be done via diffrent ways. In this demo I will use vagrant to create 3 VMs. A Master and 2 Nodes.

## Configure more nodes:

- Add an entry for each added node in ``` kubernates_setup/hosts ```



## How to use:

### 1. Creare the claster:

- make sure that you are at the same directory where "vagrant file" is and run ```vagrant up```

- This will create 3 VMs of '2G RAM and 2 CPUs'

### 2. Configure the master node and install all dependecies

- Navigate to kubernates_setup directory and run the following commands

```
ansible-playbook -i hosts master-playbook.yml
ansible-playbook -i hosts nodes-playbook.yml
```