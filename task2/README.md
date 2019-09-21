# Task2:


## About:

This folder contains:

1. vagrant file: 
    - to create VMs that will be used in the kubernetes claster.
2. kubernetes-setup directory: 
    - that contains ansible playbooks and roles which will configure the nodes and install the needed independencies.
3. deployments directory:
    - includes deployment file to deploy a pod contains all containers and service file to expose the app to the outside.



## Note 

Provisioning the infrastructure may be done via diffrent ways. In this demo I will use vagrant to create 3 VMs. A Master and 2 Nodes.

## Configure more nodes:

- Just edit Vagrantfile change N variable to any number you want.


## How to use:

#### 1. Creare the claster:

- make sure that you are at the same directory where "vagrant file" is and run ```vagrant up```

- This will create 3 VMs of '2G RAM and 2 CPUs'
- Configure the master node and install all dependecies


#### Run the deployment and service file:

1. Copy the deployment files to the master node.
2. Run the commands
```
kubectl apply -f deployments/nginx_deployment.yml
kubectl apply -f deployments/nginx_service.yml
```
3. You then can access the application using the following URL
``` 192.168.50.10:30500 ```

4. You then can access Kibana dashboard using the following URL
``` 192.168.50.10:30501 ```