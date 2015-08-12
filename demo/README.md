Make links everywhere clickable and make sure that they open in a specific window (target=...)

Run the demo with Mattias private aws account

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


# Command line example


brew install awscli

## Create AWS key & secret

From AWS Web, click My name (top right), Security Credentials.

aws configure
- Key
- Secret
- Default region eu-central-1
- Default output format json

aws ec2 run-instances --image-id ami-accff2b1 --count 1 --instance-type t2.micro --key-name netinsight --security-groups launch-wizard-1

aws ec2 describe-instances --instance-ids XXX

Ta ip-adressen från instansen vi startade tidigare

aws ec2 describe-instances --instance-ids YYY --query 'Reservations[0].Instances[0].PublicIpAddress'`

aws ec2 wait instance-status-ok --instance-ids XXX


ssh -o StrictHostKeyChecking=no ubuntu@$ip uname -a



