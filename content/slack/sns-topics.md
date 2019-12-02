---
title: "Create SNS Topics"
chapter: false
weight: 15
---

{{% notice tip %}}
Make sure you are still in the **us-east-1** (North Virginia) region.
{{% /notice %}}

1. Click on Services Drop down, type **SNS** and select **Simple Notification Service**.

1. Click on **Topics** on left-side menu. Click **Create Topic**.

1. Name: **cloudformation-alert**

1. Under **Access Policy**, select **Everyone** for both sections. Click **Create topic**.
![SNS Policy](/images/sns-policy.png)

1. Repeat the above steps to create another topic for **cloudwatch-alert**.
