---
title: "CloudFormation Notification"
chapter: false
weight: 21
---

1. Go to **CloudFormation** service. Click on Stack **chatbot-workshop-rest-api-lambda**.

1. Click on **Update**.

1. Leave Step 1 and 2 as default, click **Next**.

1. At Step 3, scroll down and click on **Notification options**. Select SNS: **cloudformation-alert**. Click **Next**.
![CloudFormation notification](/images/cfn-notification.png)

1. At Step 4 Review, check the acknowledge box and click **Update stack**.
![CloudFormation review](/images/cfn-review.png)

1. Now everytime you makes changes to your Stack, you will see alert in your Slack.
![Slack CloudFormation alert](/images/slack-cfn-alert.png)

