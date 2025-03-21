# Creating and configuring the VPC

VPC(Virtual Private Cloud) is a logically isolated network that allows you to launch EC2 instances in a public or private subnets.

## Create multiple VPC in different regions and name them accordingly. On AWS, choose VPC and more option to select the subnets as well.

- Select the number of public and private subnets where you want to launch the instances.

- Select multiple availability zones for your public and private subnets.

- If selecting private subnet, then choose NAT Gateway option so you can configure your private IP to public IP from NAT pool to communicate with servers across the web.

- **Configure the security groups for your VPC to allow required Inbound and Outbound traffic.**

  - Copy the VPC ID and paste it to the Security Groups searchbar -> Select the VPC -> Edit Inbound rules.

  - Security groups with appropriate inbound and outbound rules for:

    -**HTTP/HTTPS (ports `80/443`)**

    - **SSH (port `22`) for management**

  - **Make sure you select your IP as well to access the servers.**

## Select this VPC while creating your Target Groups as well as while creating your Launch template image.

---
