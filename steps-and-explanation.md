In this project i was able to create a virtual server make it serve webpages and also make sure it is secure, scalable, reliable and efficient using AWS. The steps involved in creating this include

- STEP 1: *create a vpc known as Virtual private cloud* 

- STEP 2: *after creating a VPC you then create an Internet Gateway (IGW) and attach it to the VPC which you have created*

- STEP 3: *after that you create a subnet (make sure this subnets are in at least two different availability zones so as not to have an issue along the way, i encountered an issue here)*

- STEP 4: *create a route table and associate it with the subnet created earlier*

- STEP 5: *edit the route table by connecting it to the IGW created earlier*

- STEP 6: *create Target group during this process you will be required to attach the vpc you created earlier*

- STEP 7: *create load balancer (i will be using Application Load Balancer (ALB) because i am installing a web server) while creating this you will need to create a security group (make sure the security group is associated with the VPC)*

- STEP 8: *create an auto scaling group and you will be required to create a launch template*

- STEP 9: *use the launch template created in the autoscaling group and create the autoscaling Group*

- STEP 10: *after the autoscaling group has been created, instances will be launched automatically depending on the stated desired capacity*

- STEP 11: *check if the the server is running properly by copyin the DNS name in the load balancer page and running it in a new tab*

- STEP 12: *to ensure the autoscaling group rules attached is effective delete one instanve and it will automatically create another one*

##CHALLENGES FACED##

while i was creating this project the challenges i encountered were

- Issue while creating the load balance: i was asked to select at least two availabilty and they must have at least one subnet in them but i had only chosen only one availability zone earlier.

- Declining subnet at the launch template advanced network setting: it kept declining any i selected. I later realised it was not necessaryto include a subnet.

## COMMAND ##

i had a command which i uesd in the User data section, i inserted it. the command is

#!/bin/bash
yes | sudo apt update yes | sudo apt install apache2
echo "<h1 »Seryer Details</h1><p><strong>Hostname:</strong> $(hostname)
</p><p><strong>IP Address:</strong> $(hostname -I | cut -d**_f1)</p>*>
/var/www/html/index.html
sudo systemctl restart apache2


