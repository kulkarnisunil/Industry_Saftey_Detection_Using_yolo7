# Industry_Saftey_Detection_Using_yolo7

## GitHub commands

1. git clone https://github.com/

2. git add .

3. git commit -m "readme updated"

4. git push origin main

5. git clone https://github.com/WongKinYiu/yolov7


## create steups

## create virtual environment

1.conda create -n isd python=3.10 -y


## Activate the environment 

2.conda activate isd

## install requirements

pip install -r requirements.txt

## Workflows

-constants

-config_entity

-artifact_entity

-components

-pipeline

-app.py


## AWS Configurations


#aws cli download link: https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

aws configure

# AWS-CICD-Deployment-with-Github-Actions

## 1.Login to AWS console

## 2.Create IAM user for deployment

#with specific access

1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


#Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

#Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess

# 3. Create ECR repo to store/save docker image

- Save the URI: _______.dkr.ecr.us-east-1.amazonaws.com/yolov7app

# 4. Create EC2 machine (Ubuntu)

# 5. Open EC2 and Install docker in EC2 Machine:

#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker

# 6. Configure EC2 as self-hosted runner:

setting>actions>runner>new self hosted runner> choose os> then run command one by one

# 7. Setup github secrets:

AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = us-east-1

AWS_ECR_LOGIN_URI = demo>>  _________.dkr.ecr.ap-south-1.amazonaws.com

ECR_REPOSITORY_NAME = simple-app
