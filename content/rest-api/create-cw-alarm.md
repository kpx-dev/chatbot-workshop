---
title: "Create CloudWatch Alarm"
chapter: false
weight: 22
---

1. Go to **CloudWatch** service. Click on **Alarms** on the left hand side. Click on **Create alarm** button.

1. Click **Select Metric** button. Look for **Lambda** and click on it. Clik on **By Function Name**. Select the one starts with prefix **chatbot-workshop-** and the Metric Name is **Errors**. Then click **Select metric**.
![CloudWatch Alarm metric](/images/cw-alarm-error.png)

1. Update the Metric panne to set Statistic: **Sum**, Period: **1 minute**
![CloudWatch Alarm metric setting](/images/cw-alarm-metric-setting.png)

1. Under the Conditions pane, update the value for the threshold value to **1** and click **Next**.
![CloudWatch Alarm metric conditions](/images/cw-alarm-conditions.png)

1. Under the Notification pane, select the SNS topic: **cloudwatch-alert**. Then click on **Add notification**.
![CloudWatch Alarm metric conditions](/images/cw-alarm-notification.png)

1. Select **OK** and select the same SNS topic **cloudwatch-alert**. Then click **Next**.
![CloudWatch Alarm metric conditions](/images/cw-alarm-ok.png)

1. Name the alarm **chatbot-workshop-lambda-error**, click **Next** and **Create alarm**.
