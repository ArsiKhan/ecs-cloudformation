# Deploy containers using Elastic Container Service and CloudFormation

The templates in this repo are best suited for a basic web architecture of an application with a frontend and backend service.

To use these templates launch a cluster template for the launch type and networking stack that you want. Then launch a service template for each service you want to run in the cluster. When launching a service template its important to make sure the "StackName" value is filled in with the same name that you selected for the name of your cluster stack.

# Steps
1. First launch a Cluster Template which creates the depedencies for the ECS Service
2. Once the Cluster is launched, use the Service Template to Launch 2 services in the Cluster
3. For validating the templates, use validate.sh in the tests Directory
