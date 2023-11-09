# Cloud Formation Templates to Deploy Fargate Tasks in a Default VPC on a Public Subnet 

## We are going to build below setup using CloudFormation Tempalte 

<img src="https://github.com/sbanala12/AWS-CFT-Templates/blob/sbanala12-ECS/misc_files/Ecs_setup.png" width="1000" height="400">

## Prerequsites

 - AWS account  
 - Registered Domain name  ( ex: training.com) 
 - SSL certificate 
 - IAM role with privilege accees with AWS Access Key ID and AWS Secret Access Key 
 - AWS CLI to install locally 


## Step 01 - update ECS_params.json file 

  - To create a local copy of the repository, please execute the "git clone" command with the repository's URL
      ## git clone  https://github.com/sbanala12/AWS-CFT-Templates.git
  - To navigate to the AWS_ECS folder from the command line, you will use the cd (change directory) 
    command followed by the path to your AWS_ECS folder If the folder is in your current directory, you can simply do: 
      ## cd AWS_ECS
  - Please update the ECS_params.json file with the appropriate parameter values as per your requirements. 

## Step 02 - To authenticate the AWS account

   - To authenticate your AWS account from the command line, use the 'aws configure' command to set up your credentials.

  $ aws configure 
  ##### AWS Access Key ID [****************PTWV]: 
  ##### AWS Secret Access Key [****************MjpZ]:
  ##### Default region name [us-east-1]: us-east-1  
  
## Step 03 - Deploy Cloudformation Template 

- To deploy a CloudFormation stack and specify the name of the stack, use the AWS CLI command 
      'aws cloudformation create-stack' followed by the --stack-name parameter with your desired stack name. Here's an example:

   ## aws cloudformation deploy --template-file .\ECS.yml --stack-name <YourStackName> --region us-east-1 --capabilities CAPABILITY_NAMED_IAM CAPABILITY_AUTO_EXPAND --parameter-overrides file://ECS_params.json

 - Replace YourStackName with the actual name you want to give your stack

  
      
      



