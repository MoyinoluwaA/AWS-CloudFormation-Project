### Project Title - Deploy a high-availability web app using CloudFormation
This project is one of the projects done during the Udacity Cloud DevOps nanodegree. It deploys a high-availability web app using CloudFormation script. This folder contains the following files:

#### network.yml
Here, the networking infrastructure such as VPC and Public and Private Subnets were created. 

#### server-parameters.json
The JSON file is used for storing the CIDR for vpc and subnets. 

#### final-project.yml
Here, the CloudFormation code uses this YAML template for building the cloud infrastructure, as required for the project. 

#### server-parameters.json
The JSON file is used for increasing the generic nature of the YAML code to make the template reusable. For example, the JSON file contains a "ParameterKey" as "EnvironmentName" and "ParameterValue" as "UdacityProject". 
In YAML code, the `${EnvironmentName}` would be substituted with `UdacityProject` accordingly.

#### script files
These are used to quickly spin up the cloudformation stacks.

### To Replicate
- Log in to aws cli
- Change the region in the script files if you will not be using `us-east-1`
- cd into `scripts` folder and run `./create-network.sh` to deploy network infrastructure
- Allow for all the resources to be created completely. Then, run `./create.sh` to deploy the Auto scaling group and load balancer
- Check the export for the load balancer url and navigate to the url or append index.html if nothing is displayed
- `It works! Udagram, Udacity` would be displayed on the screen if properly set up
- Remember to delete the stack when done using the `delete-stack` command.