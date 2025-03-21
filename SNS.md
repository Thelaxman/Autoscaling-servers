# 📩 AWS SNS Configuration with Auto Scaling Groups

## 📝 Description

The steps to set up Amazon Simple Notification Service (SNS) with Auto Scaling Groups (ASG) to receive notifications when scaling events occur.

## ⚙️ Configuration Steps

1. **Creating an SNS Topic**

   - Navigate to the **AWS Management Console**.
   - Go to **SNS -> Topics**.
   - Click on **Create topic**.
   - Select **Standard** as the topic type.
   - Enter a **Name** for the topic (e.g., `autoscaling-alerts`).
   - Click **Create topic**.

2. **Creating a Subscription**

   - Click on the newly created topic.
   - Go to the **Subscriptions** tab and click **Create subscription**.
   - Choose **Protocol** as **Email**.
   - Enter your **Email Endpoint**.
   - Click **Create subscription**.
   - Check your email and **confirm the subscription**.

3. **Configuring ASG Notifications**
   - Go to **EC2 -> Auto Scaling -> Auto Scaling Groups**.
   - Select the desired Auto Scaling Group.
   - Go to the **Notifications** tab and click **Add notification**.
   - Choose the **SNS topic** created earlier.
   - Select the scaling events you want to be notified about (e.g., Instance Launch, Instance Terminate).
   - Click **Save changes**.

## ✅ Verification

- Trigger a scaling event by manually increasing or decreasing capacity.
- Check your email for notifications from SNS about the scaling activities.

---
