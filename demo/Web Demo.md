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

The Security group shall be named launch-wizard-1 for the cli demo to work.

Launch

Main menu - Instances

Show Networking-slide while the instance starts

ssh ubuntu@...

sudo apt-get update
sudo apt-get install apache2

Leave the instance running
