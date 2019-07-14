# Deploy containers using Elastic Container Service and CloudFormation

The templates in this repo are best suited for a basic web architecture of an application with a frontend and backend service.

To use these templates launch a cluster template for the EC2Launch type and networking stack that you want. Then launch a service template for each service you want to run in the cluster. When launching a service template its important to make sure the "StackName" value is filled in with the same name that you selected for the name of your cluster stack.

# Steps

1. Clone the Github repo
2. Browse to the EC2LaunchType/clusters
3. Upload the file to a location such as S3 Bucket from where CloudFormation could use the template
4. Create the Cluster with values as per your liking. The following resources would be created in this step:
   - A VPC
   - 3 Public Subnets
   - One IGW with Subnets Association with the public subnets
   - 1 ECS Cluster with Autoscaling Group and Security Groups
   - 1 ECS role for EC2 Instances
   - One ALB with the required Security Groups and Target Groups
 5. Browse to the EC2LaunchType/services directory for deploying the ECS services and Task Definitions
 6. Create the Services with values as per your liking. The following resources would be created in this step:
   - 2 ECS services
   - 2 Task Definitions
   - The second Service Target Group
   - ALB rules for directing traffic to appropriate services
  
