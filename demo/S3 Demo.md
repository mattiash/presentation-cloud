# S3 Demo

Show bucket backup.holmlund.se i s3-webben.

Can upload / download files via web

host backup.holmlund.se - show output

s3cmd ls
s3cmd ls s3://backup.holmlund.se
echo test > test.txt
s3cmd put test.txt s3://backup.holmlund.se/

http://backup.holmlund.se/test.txt
