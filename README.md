Depolying a Simple Crud Node.js Application using ECS with Fargate in AWS

ECS is a managed container orchestrator like Kubernetes and Swarm. Orchestrator manages the lifecycle of containers(create, restart, destroy), then deploy and load balance the application across multiple servers, autoscaling to handle the variance in traffic, roll out changes to the application. ECS is a simpler alternative to EKS, Swarm.

ECS has two launch types a) EC2 Type and b) Fargate

** EC2 Type: **
We have to manage the underlying EC2 Instances, and we have full control over the infratructure. ECS manages the containers in EC2 Instances

** Fargate: **
AWS manages the underlying infrastructure. It follows a serverless architecture, it will create servers on demand, no need to provision/manage the servers. You only pay for what you use.

** ECS Task Definition: ** is a blueprint of the configuration(CPU, memory, images, ports, volumes), describes how containers should launch.
 
** ECS Tasks: ** An instance(s) of a Task Definition. A running container(s) with the settings defined in Task Definition

** ECS Services: ** ensures a certain number of Tasks are running at all times, Restarts Containers that have exited/crashed, EC2 Instance fails, it will restart task on a working EC2 instance.

** Load Balancers: ** routes the traffic to the service
