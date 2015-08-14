# AWS Web EC2

## Preparation

AWS Login page

Show regions dropdown in upper right corner. Select Frankfurt.

Click "0 Key Pairs"

"Import Key Pair"

Key pair name: netinsight

Paste content of ~/.ssh/netinsight.pub


## Create Instance

EC2 Dashboard

Click Launch Instance

Ubuntu 14.04

Select t2.micro, Review and Launch.

Edit security groups, Open port 80

Launch

Main menu - Instances

ssh ubuntu@...

sudo apt-get update
sudo apt-get install apache2


Låt instansen köra vidare!


# aws cli


brew install awscli

Use two terminals side by side. Start ./run-instance in the right terminal


## Create AWS key & secret

From AWS Web, click My name (top right), Security Credentials.

aws configure
- Key
- Secret
- Default region eu-central-1
- Default output format json

## Run instance

aws ec2 describe-instances

aws ec2 describe-instances --query Reservations[0].Instances[0].PublicIpAddress

# S3 Demo

Show bucket backup.holmlund.se i s3-webben.

Can upload / download files via web

host backup.holmlund.se - show output

s3cmd ls
s3cmd ls s3://backup.holmlund.se
echo test > test.txt
s3cmd put test.txt s3://backup.holmlund.se/



