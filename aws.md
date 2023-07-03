# AWS – Week 5

### Differences between AWS and Azure

### AWS	
-	Not necessary to use 
-	By Default IP address is dynamic meaning it changes it everytime VM restarts.
-	Launch instance to create VM	

### Azure
-	Everything has to go to Resource Group
-	By Default the Ip address is static meaning Public ip address remains same when VM starts
-	Create VM 

## **AWS Introduction**
Amazon Web Services (AWS) is a cloud computing platform that offers a wide range of services, including EC2 (Elastic Compute Cloud). EC2 allows you to launch and manage virtual servers in the cloud.

1. Sign in to the AWS Management Console: Go to the AWS Management Console (https://console.aws.amazon.com/) and sign in to your AWS account.


2. Navigate to EC2: From the AWS Management Console, search for and select "EC2" to access the EC2 Dashboard.


3. Choose an AMI (Amazon Machine Image)


4. Choose an Instance Type


5. Configure Network Settings


6. Configure Security Groups


7. Configure Storage


### How to create ssh keypair on AWS

1. Search for "key pair" on search and select key pair (EC2 feature)


2. Select "create key pair" on top right 


3. Give a key pair name


4. Select the key pair type (RSA)


5. Select the format of key file (.pem)


6. Create the key file. 

#### After you create the key pair it will generate the keypair and will download the .pem file consist of private key with the .pem extension. 


### How to SSH into an EC2 Instance

1. Locate the Instance: From the EC2 dashboard, find the EC2 instance you want to connect. 


2. Open Git Bash terminal


3. Change Directory (cd into home directory)


4. Set Permissions on Key Pair- Chmod 400


5. Copy the path and enter into the Terminal.


### How to terminate an EC2 instance

1. Sign in to the AWS 


2. Navigate to EC2


3. Locate the Instance


4. Select the Instance


5. Terminate Instance


6. Confirm Termination


7. Termination Status

### Script for the app

#!/bin/bash

1. #### update source list
sudo apt update -y

2. #### upgrade all the packages and installs them in the kernal
sudo apt upgrade -y

3. #### install nginx
sudo apt install nginx -y

4. #### Start nginx on boot
sudo systemctl enable nginx

5. #### start nginx
sudo systemctl start nginx

6. #### restart nginx
sudo systemctl restart nginx

7. #### enable nginx - auto runs on startup
sudo systemctl enable nginx

8. #### add proxy command
sudo sed -i 's|try_files $uri $uri/ =404;|proxy_pass http://localhost:3000;|' /etc/nginx/sites-available/default

9. #### restart nginx
sudo systemctl restart nginx

10. #### enable nginx - auto runs on startup
sudo systemctl enable nginx

11. #### download node js
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -

12. #### add in env
export DB_HOST=mongodb://63.33.164.191:27017/posts

13. #### install node js
sudo apt install nodejs -y

14. #### update source list
sudo apt update -y

15. #### install pm2
sudo npm install -g pm2

16. #### git clone app
git clone https://github.com/jungjinggg/tech241_sparta_app app2

17. #### get into app folder
cd ~/app2/app

18. #### install node js inside folder
npm install -y

19. #### start app
pm2 start app.js --name "sparta app"


### Script to run DB

#!/bin/bash

# Update and upgrade the system
sudo apt update -y

sudo apt upgrade -y

# Install the correct version of MongoDB (version 3.2.x)

wget -qO - https://www.mongodb.org/static/pgp/server-3.2.asc | sudo apt-key add -

echo "deb http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mong$sudo apt update -y

sudo apt-get install -y mongodb-org=3.2.20 mongodb-org-server=3.2.20 mongodb-org-shell=3.2.20 mongodb-org-mongos=3.2.20$

####  Configure MongoDB to accept connections from the app VM

sudo sed -i 's/bindIp: 127.0.0.1/bindIp: 0.0.0.0/g' /etc/mongod.conf

#### Start and enable MongoDB
sudo systemctl start mongod

sudo systemctl enable mongod

After Running Both Script and working


![img_4.png](img_4.png)

![img_5.png](img_5.png)