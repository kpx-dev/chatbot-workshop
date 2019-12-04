---
title: "Configure AWS Chatbot"
chapter: false
weight: 16
---

1. Click on Services Drop down, type **Chatbot** and select AWS Chatbot. Select **Slack** as the chat client from the dropdown. Click on **Configure client**.
![Select Chat Client](/images/select-chat-client.png)

1. Create a new Slack workspace or Login with your existing Slack workshop where you have **Admin** access to create channels.

1. Once Logged into Slack, click on **Allow** AWS Chatbot to access your Slack workspace
![Slack Permission](/images/slack-perm.png)

1. Go to **Slack**, create 2 public channels: **cloudformation-alert**, **cloudwatch-alert**.
![Create Slack Channel](/images/create-slack-channel.png)

1. Go back to AWS Console. Click on Refresh icon, you should now see 2 new Slack channels. Channel type: **Public**.
![Select Slack Channel](/images/select-slack-channel.png)

1. IAM Role: **Create an IAM role using a template**. Permission Role Name: **AWSChatbot-Slack-Cloudformation-role**. Policy templates: **Notification permissions**
![Create Role](/images/permission-role-name.png)

1. Under Notifcations section, Region: **US East - N Virginia**. Topics: **cloudformation-alert**. Click **Configure**.
![Chatbot SNS Topics](/images/chatbot-sns-topic.png)

1. Repeat from **Step 4** above to setup **cloudwatch-alert**.
