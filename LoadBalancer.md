# 🏗️ AWS Application Load Balancer (ALB) Configuration for Autoscaling Project

## 📝 Description

The steps to set up an Application Load Balancer (ALB) in AWS and attach the previously created Target Group to distribute traffic to the auto-scaled EC2 instances.

## ⚙️ Configuration Steps

1. **Creating the Application Load Balancer**

   - Navigate to the **AWS Management Console**.
   - Go to **EC2 -> Load Balancing -> Load Balancers**.
   - Click on **Create Load Balancer**.
   - Select **Application Load Balancer**.
   - Enter a **Name** for the load balancer (e.g., `autoscaling-alb`).
   - Choose **Internet-facing** for the **Scheme**.
   - Select **IPv4** for **IP address type**.

2. **Network Mapping**

   - Choose the **VPC** where your instances are located.
   - Select **Availability Zones** and corresponding **subnets** for high availability.

3. **Listeners and Routing**

   - Add a **Listener** with the following settings:
     - **Protocol:** HTTP
     - **Port:** 80
   - Select the **Default Action** as **Forward to Target Group**.
   - Choose the previously created **Target Group** from the dropdown list.

4. **Security Groups**

   - Select an existing security group or create a new one.
   - Ensure that **HTTP (port 80)** traffic is allowed.

5. **Review and Create**
   - Review the settings and click **Create Load Balancer**.
   - Wait for the ALB status to change to **Active**.

## ✅ Verification

- Access the **DNS name** of the load balancer from the AWS Console.
- Test the connection by visiting the DNS name in a browser (e.g., `http://autoscaling-alb-1234567890.us-east-1.elb.amazonaws.com`).
- Verify that traffic is being routed to one of the instances.

---
