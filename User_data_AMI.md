# User Data

User data in AWS enables you to automate and customize the setup of EC2 instances by running scripts or commands during instance launch.

How to create User Data on AWS
1. **Sign in to the AWS Management Console**


2. **Navigate to EC2**: From the AWS Management Console, search for and select "EC2" to access the EC2 Dashboard.

![Alt text](<EC2 Dashboard.png>)


3. **Select Instance and choose Lauch Instance**

![Alt text](<Launch Instance.png>)

4. **Choose Amazon Machine Image**

![Alt text](<Choose Image.png>)

5. **Select Instance Type**

![Alt text](<Select Instance.png>)

6. **Configure Network Settings and Security Groups**

![Alt text](<Configure Network.png>)


7. **Configure Storage**

![Alt text](<security group.png>)

8. **Go to Advanced setting and go to User data and paste the DB script then Launch Instance**

![Alt text](<User data.png>)


# Amazon Machine Image (AMI)

AMI is snapshot of the disk by making a copy to recreate a virtual machine.  By making an image this disk then can be used to recreate the first VM so its virtually identical copy of a VM. 


### Why make AMI?

Creating an AMI in AWS allows you to capture the state of an EC2 instance, providing a reusable template for launching identical instances. AMIs offer benefits such as reproducibility, faster deployment, improved disaster recovery capabilities.

- It costs less than having a Virtual Machine Running.

- It is only using the disk space.


### How to create AMI?

1. Go to Instance

![Alt text](<EC2 Dashboard.png>)

2. Select the Instance you want to use

3. Select action on top right.

4. Select Image and templete and choose create Image option

![Alt text](<Creating AMI.png>)

5. Add image name and description

![Alt text](<Add image name and description.png>)

6. Add new tag and add key and value and Launch Instance. 
   
![Alt text](<Add new tag.png>)





