
#!/bin/bash

# get Admin privillages
sudo su

# Install httpd (Linux 2 version)

yum update -y
yum install -y httpd.x86_64
systemctl start httpd.service
systemctl enable httpd.service
echo "Hello Welcome to EC2 $(hostname -f)" > /var/www/html/index.html
