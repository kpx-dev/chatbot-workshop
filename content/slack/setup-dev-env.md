---
title: "Setup Dev Env with Cloud9"
chapter: false
weight: 14
---

1. Login to your AWS Account, make sure you are in the **North Virginia (us-east-1)** region

1. Click on Services Drop down, type **Cloud9**. Click on **Create environment**.

1. Type: **chatbot-workshop** for Name. Click on **Next step**.

1. Leave all settings default. Click on **Next step**. Then click **Create environment**.
![Cloud9](/images/cloud9.png)

1. It will take about 3-5 minutes to create your Cloud9 environment.

1. We'll deploy a simple REST API service. From your Cloud9, open a new Terminal (+ icon next to Welcome tab) and run:
```shell
git clone https://github.com/kienpham2000/lambda-example.git && cd lambda-example
```

1. Output will look like this
```shell
user:~/environment $ git clone https://github.com/kienpham2000/lambda-example.git && cd lambda-example
Cloning into 'lambda-example'...
remote: Enumerating objects: 52, done.
remote: Counting objects: 100% (52/52), done.
remote: Compressing objects: 100% (37/37), done.
remote: Total 52 (delta 23), reused 39 (delta 13), pack-reused 0
Unpacking objects: 100% (52/52), done.
user:~/environment/lambda-example (master) $
```

1. Install packages (SAM, httpie, etc.). Press **Enter** to continue. This will take about 2-3 minutes.
```shell
./install-packages.sh
```
