---
title: "Package & Deploy Lambda using SAM"
chapter: false
weight: 21
---

1. Go back to **Cloud9** service.

1. Create the S3 repo to store SAM artifact. Since the S3 repo name must be ***globally unique***, please postfix with your username
```
aws s3api create-bucket --bucket chatbot-workshop-[your-username]
```

1. Make sure you are in the **rest-api** directory
```
cd ~/environment/lambda-example/rest-api/
```

1. Package the template. Don't forget to replace `chatbot-workshop-[your-username]` with your actual S3 bucket name.
```
sam package --output-template-file template_packaged.yaml --s3-bucket chatbot-workshop-[your-username]
```

1. Deploy Lambda using SAM. This will take 1-2 minutes as SAM is creating CloudFormation stack. You will also see that there's a new S3 bucket created by SAM.
```
sam deploy --template-file template_packaged.yaml --stack-name chatbot-workshop-rest-api-lambda --capabilities CAPABILITY_IAM
```

1. Once Deployment is done, there will be a CloudFront url for your endpoint.
![Sam Deploy](/images/sam-deploy.png)

1. Test that endpoint url using curl or http and it should be working
```shell
http https://xxx.execute-api.us-east-1.amazonaws.com/Prod/
```

1. Now to go **CloudFormation** service from the main Service dropdown.

1. Click on the Stack Name: **chatbot-workshop-rest-api-lambda**. Click **Update**.

1. Click **Next** 2 times to get to Step 3. Expand the: **Notification options**. Select **cloudformation-alert** SNS. Click **Next**.
![CloudFormation Notify SNS](/images/cfn-sns.png)

1. Check the acknowledge box and click **Update stack**. Once done, you should receive notification to your Slack channel from now.
