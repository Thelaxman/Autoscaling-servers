# 🌐 AWS Route 53 Configuration for Autoscaling Project

## 📝 Description

The steps to configure Amazon Route 53 to manage domain names and route traffic to the Application Load Balancer (ALB) used in the Autoscaling Servers Project.

## ⚙️ Configuration Steps

1. **Creating a Hosted Zone**

   - Go to the **AWS Management Console**.
   - Navigate to **Route 53 -> Hosted Zones**.
   - Click on **Create hosted zone**.
   - Enter your **Domain Name** (e.g., `example.com`).
   - Choose **Public Hosted Zone**.
   - Click **Create hosted zone**.

2. **Creating an ALB DNS Record**

   - In the hosted zone, click on **Create record**.
   - Choose **Simple routing**.
   - Click **Define simple record**.
   - Set **Record Name** (e.g., `www`).
   - Select **Record Type** as **A - IPv4 address**.
   - Choose **Alias** as **Yes**.
   - In the **Alias Target**, select your **Application Load Balancer** from the list.
   - Click **Create records**.

3. **DNS Propagation**
   - Update your domain’s **NS records** at your domain registrar to point to the Route 53 nameservers.
   - Allow some time for DNS propagation.

## ✅ Verification

- Visit your domain (e.g., `www.example.com`) to ensure it correctly resolves to the ALB.
- Test the setup by stopping and starting instances to confirm autoscaling works as expected.

---
