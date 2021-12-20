## Project Title - Deploy a high-availability web app using CloudFormation

The objectve of this project is to beSparkify is a music streaming company that collects data on songs and user activities. The objectives of this project is to create an ETL data pipline for the company that extracts data from S3, stages them in Redshift so that the songs and user activities data can be easily queried and analyzed to make informed decisions.

I created a diagram with Lucid chart as a visual aid to understand my CloudFormation script.

I wrote a CloudFormation script called final-project-starter.yml. This contains the commands for all the services/ applications that need to be created.

I obtained Sparkify's existing data from two directories containing JSON files containing songs and activities data in S3.

For this project, I created the following files:
- final-project-starter.yml: This is the CloudFormation script that contains the commands for all the services/ applications that need to be created, dependencies and outputs for the stack
- server-parameters.json: This contains the parameters to be used in the CloudFormation script
- create.sh: This is the shell script that executes to create CloudFormation stack with the script
- update.sh: This is the shell script that updates an existing stack when an update is made to the CloudFormation script

# Steps taken
I started by reading the requirements for Udagram project and I created a diagram based on all the services/ applications that will be needed for the project. After the diagram was completed, I created both the CloudFormation script and the parameter file. I added resources to the script one after the other and I ran the update script, looked at the console to make sure both the stack and the necessary resources were created.
Below are the resources created:
- Role to which S3 permission policy was attached
- Policy for the role
- Instance profile
- VPC
- Internet Gateway
- Internet Gateway attachment
- Two public subnets in different Availability Zones
- Two private subnets in different Availability Zones
- Two NA Gateways and EIPs
- Public and private Route table, Route and Association
- Load Balancer
- Load Balancer Security Group
- Web Server Security Group 
- Application Launch Configuration
- Listener and Listener Rule

After creating all the necessary resources, I created a jumpbox, SSHed into it in order to connect to the application on the private subnet

In the same folder as this file are some snapshots that show the steps I took in the project.

LoadBalancerURL is http://temit-udagr-1xiu7grlv365k-1816528381.us-west-2.elb.amazonaws.com/