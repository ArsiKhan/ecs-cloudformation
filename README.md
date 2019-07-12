# Deploy containers using Elastic Container Service and CloudFormation

The templates in this repo are best suited for a basic web architecture of an application with a frontend and backend service.

To use these templates launch a cluster template for the launch type and networking stack that you want. Then launch a service template for each service you want to run in the cluster. When launching a service template its important to make sure the "StackName" value is filled in with the same name that you selected for the name of your cluster stack.

# Pre-requisites
