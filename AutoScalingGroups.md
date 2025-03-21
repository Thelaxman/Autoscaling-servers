# 🚀 AWS Auto Scaling Group Configuration for Autoscaling Project

## 📝 Description

This document provides the steps to create an Auto Scaling Group (ASG) in AWS that uses the AMI with the Docker container running the React website. The ASG will use the existing Target Group and Application Load Balancer (ALB) to manage and scale EC2 instances automatically.

## ⚙️ Configuration Steps

1. **Creating the Auto Scaling Group**

   - Navigate to the **AWS Management Console**.
   - Go to **EC2 -> Auto Scaling -> Auto Scaling Groups**.
   - Click on **Create Auto Scaling group**.
   - Enter a **Name** for the Auto Scaling Group (e.g., `autoscaling-asg`).
   - Select the **Launch Template** that uses the preconfigured AMI with the Docker container.

2. **Network and Load Balancer Settings**

   - Choose the **VPC** and **Subnets** that the ASG should use.
   - Attach the **Application Load Balancer** created earlier.
   - Choose the **Target Group** to route the traffic.

3. **Group Size and Scaling Policies**

   - Set **Desired Capacity**, **Minimum Capacity**, and **Maximum Capacity** as needed (e.g., 2, 1, and 5 respectively).
   - Choose **Target tracking scaling policy** to adjust capacity based on CPU utilization or other metrics.

4. **Health Checks**

   - Enable **ELB health checks** to ensure instance availability.
   - Set the **Health check grace period** to a reasonable value (e.g., 300 seconds).

5. **Review and Create**
   - Review all settings and click **Create Auto Scaling group**.
   - Monitor the instances to ensure they are launched and registered with the load balancer.

## ✅ Verification

- Check the **Auto Scaling Group** to ensure instances are healthy and running.
- Stop one of the instances manually to verify automatic replacement.
- Access the **Load Balancer DNS** to ensure traffic routing to the new instance.

---
