---
title: "Trigger CloudWatch Alarm"
chapter: false
weight: 24
---

### Trigger OK Alarm

1. Go back to **Cloud9** service.

1. Go into the sample REST API service code:
```
cd /home/ec2-user/environment/lambda-example/rest-api
```

1. Package your Lambda
```
sam package --output-template-file template_packaged.yaml --s3-bucket chatbot-workshop-[your-username]
```

1. Deploy your Lambda. After about 30 seconds, you should see a Slack message in your **cloudwatch-alert** channel saying everything is OK.
```
sam deploy --template-file template_packaged.yaml --stack-name chatbot-workshop-rest-api-lambda --capabilities CAPABILITY_IAM
```

![Slack Ok](/images/slack-ok.png)

### Trigger Error Alarm

1. Modify the file **rest-api.js**
```
vi rest-api.js
```

1. Enable a line that would break the service so that CloudWatch Alarm will trigger.
```
const payload = {};
```

1. Package your Lambda
```
sam package --output-template-file template_packaged.yaml --s3-bucket chatbot-workshop-[your-username]
```

1. Deploy your Lambda. After about 30 seconds, you should see a Slack message in your **cloudwatch-alert** channel saying everything is OK.
```
sam deploy --template-file template_packaged.yaml --stack-name chatbot-workshop-rest-api-lambda --capabilities CAPABILITY_IAM
```

1. Now try to curl your endpoint a few times. It should give you 500x error.

![Slack Error](/images/slack-error.png)
