# AWS ECS and ECR

## AMAZON EC2 CONTAINER REGISTRY (AMAZON ECR) 

* Fully managed **docker container registry**
* **Store, manage, and deploy container image**s
* Integrated with amazon ECS
* **Encrypted, redundant, and highly-available**
* **Granular security permissions with AWS IAM** 

![Alt Image Text](images/8_1.jpg "body image")


## Amazon ECS (EC2 Container Service)

* Supports Docker containers 
* Easily run applications on a managed cluster of EC2 instances 
* Launch or stop container-enabled applications 
* Query the complete state of your cluster 
* Access familiar features
  * Security groups
  * Elastic Load Balancing 
  * EBS volumes
  * IAM roles


![Alt Image Text](images/8_6.jpg "body image")


## Key Components: 

### Container Instances 

* Amazon EC2 instances 
* Docker daemon 
* Amazon ECS agent 
 

### AMAZON ECS AGENT 

* Manages the state of containers on a single EC2 instance
* **How ECS communicates with the docker daemon on the EC2 instance**
* **Must be on every EC2 instance in your ECS cluster**
* Included with the ecs-optimized amazon machine image (AMI) 


## Key Components: Clusters 

* Resource pool
* Start empty
* dynamically scalable 
* GroupinG of container instances 


### AMAZON ECS CLUSTER

* **Logical group of amazon EC2 instances that you can place containers onto**
* Can utilize **on-demand, spot, or reserved EC2 instances**
* Can include different EC2 instance types region-specific
* **EC2 instances are linked in a virtual private cloud (VPC)**

## Key Components: Task Definitions

![Alt Image Text](images/8_2.jpg "body image")


### AN AMAZON ECS TASK DEFINITION SPECIFIES

* Docker image for each container
* CPU and memory requirements for each container
* **Links between containers**
* Networking and port settings
* Data storage volumes
* **Security IAM role**

![Alt Image Text](images/8_3.jpg "body image")

![Alt Image Text](images/8_4.jpg "body image")

![Alt Image Text](images/8_5.jpg "body image")


* Unit of Work 
* Grouping of relates containers 
* Run on container instances 


## RUN-TASK 

* **FINDS EC2 INSTANCES IN CLUSTER THAT MEET REQUIREMENTS IN THE TASK DEFINITION**
* **DEFINES HOW TASKS ARE DISTRIBUTED ONTO EC2 INSTANCES IN THE CLUSTER** 
* COMMUNICATES WITH ECS-AGENT AND DOCKER DAEMON TO RUN CONTAINERS ON ELIGIBLE EC2 INSTANCES IN THE CLUSTER 
* CAN BE EXECUTED VIA THE ECS CONSOLE, CLI, OR APIS 


## SERVICES

* Manage long-running workloads
* Automate the 'run-task' process
* Actively monitor running tasks
* Restart tasks if they fail

### SERVICE UPDATES 

* AUTOMATICALLY STARTS NEW TASKS AND STOPS OLD TASKS 
* **KEEPS THE SERVICE RUNNING DURING DEPLOYMENT** 
* **HEALTH CHECKS ENSURE NEW TASKS ARE STABLE BEFORE OLD TASKS ARE STOPPED** 
* USE THE CONSOLE, CLI, OR APIS 


## TASK PLACEMENT STRATEGY 

* DEFINES HOW TASKS ARE DISTRIBUTED ONTO EC2 INSTANCES IN THE CLUSTER

### STRATEGIES INCLUDE:

* Balance tasks for availability
* Pack tasks for efficiency
* Run **only one task per ec2 instance**
* Custom task placements


## ECS LAB


![Alt Image Text](images/8_7.jpg "body image")

![Alt Image Text](images/8_8.jpg "body image")

![Alt Image Text](images/8_9.jpg "body image")

![Alt Image Text](images/8_10.jpg "body image")

![Alt Image Text](images/8_11.jpg "body image")

