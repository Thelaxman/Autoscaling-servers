# 🎯 AWS Target Group Configuration for Autoscaling Project

## 📝 Description

The Target Group is associated with the Application Load Balancer (ALB) to distribute incoming traffic to the auto-scaled EC2 instances.

## ⚙️ Configuration Steps

1. **Creating the Target Group**

   - Navigate to the **AWS Management Console**.
   - Go to **EC2 -> Load Balancing -> Target Groups**.
   - Click on **Create target group**.
   - Choose **Instances** as the target type.
   - Enter a **Name** for the target group (e.g., `autoscaling-tg`).
   - Set the **Protocol** to **HTTP** and **Port** to **80**.
   - Choose the **VPC** where your instances are located.
   - Select **Health Check Protocol** as **HTTP** and **Path** as `/`.

2. **Health Check Settings**

   - Set **Healthy threshold** to `3`.
   - Set **Unhealthy threshold** to `2`.
   - Set **Timeout** to `5` seconds.
   - Set **Interval** to `30` seconds.
   - Optional: Adjust **Success Codes** (default is `200`).

3. **Registering Targets**
   - Select the **Instances** to include in the target group.
   - Click **Include as pending**.
   - Click **Create target group**.

## ✅ Verification

- Check the **target group status** to ensure the targets are registered and healthy.
- Test the configuration by accessing the Load Balancer's public DNS and verifying the response from one of the instances.

---
