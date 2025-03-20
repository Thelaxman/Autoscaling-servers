# Autoscaling Servers 

Autoscaling servers plays a cruical role when it comes to system avaliablity and scalabilty.
It helps in handling requests that can be on the higher side of the scale by adding more servers to the existing ones and thus balancing the traffic across them using Load balancer or proxy servers.

## Autoscaling Groups on AWS

On AWS, we also have a similar feature that we will use in this project. AWS offers both Horizontal and Vertical autoscaling :
- Horizontal Autoscaling: adding/removing servers as per system load/traffic.
- Vertical Autoscaling: increasing/decreasing the power of a single server.

## 🛠️ Prerequisites

1. **AWS Account**
   - Ensure you have an active AWS account with sufficient permissions to create and manage EC2 instances, load balancers, auto-scaling groups, and related services.

2. **AWS CLI (Command Line Interface)**
   - Installed and configured with appropriate credentials.
   - [AWS CLI Installation Guide](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)

3. **IAM Roles and Policies**
   - Necessary roles with permissions for:
     - **Auto Scaling**
     - **EC2 Instances**
     - **Elastic Load Balancing**
     - **CloudWatch Monitoring**

4. **VPC and Subnets**
   - A VPC with public and private subnets configured.
   - Ensure that subnets are in **multiple availability zones** for high availability.

5. **Key Pair**
   - An EC2 key pair to securely access the instances.
   - [Creating a Key Pair](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html)

6. **Security Groups**
   - Security groups with appropriate inbound and outbound rules for:
     - **HTTP/HTTPS (ports 80/443)**
     - **SSH (port 22) for management**

7. **Load Balancer**
   - An **Elastic Load Balancer (ELB)** configured to distribute traffic across instances.

8. **Launch Template or Configuration**
   - A template defining the instance type, AMI, security groups, and startup scripts.

9. **Auto Scaling Policies**
   - Defined scaling policies for:
     - **Target tracking (e.g., CPU utilization)**
     - **Step scaling**
     - **Scheduled scaling**

10. **Monitoring and Logging**
    - Set up CloudWatch for monitoring metrics and logging.

---

Let me know if you need more sections or adjustments! 😄
