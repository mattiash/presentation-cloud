# aws cli


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

