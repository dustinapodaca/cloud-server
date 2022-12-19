# Project: Cloud Server Deployment with AWS EC2
### Author: Dustin Apodaca
---
## Problem Domain

- Deploy a Node.js server to AWS EC2.
  - Express Server code created and used to deploy found [here](./exampleServerDeployed/).

## Processes

### GUI Process for AWS EC2 Deployment

Link to [GUI Deployment](http://expresslysimple-env.eba-a3xtkyx4.us-west-2.elasticbeanstalk.com/).

- Create an AWS account
  - [AWS Free Tier Account](https://aws.amazon.com/free/)
- Create an EC2 instance
- Specify the instance type
- Specify the Environment
  - Node.js Server
- Zip the files to be deployed
- Upload the zip file to the EC2 instance
- Start the server

### CLI Process for AWS EC2 Deployment

Link to [CLI Deployment](http://basic-express-server-dev.us-west-2.elasticbeanstalk.com/).

- Install the AWS CLI on your local machine
  - Using [Homebrew](https://brew.sh/):
    - `brew install awscli`
    - `aws --version`
  - Install the Elastic Beanstalk CLI tools
    - `brew install awsebcli`
    - `eb --version`
- Create a new Access Key for your AWS account from the AWS Management Console
  - [AWS IAM](https://console.aws.amazon.com/iam/home)
  - Ensure you securely store the Access Key ID and Secret Access Key in a safe place
- Configure the AWS CLI with your AWS Access Credentials and region
  - `aws configure`
- From inside the root directory of your Node.js application:
  - Initialize the AWS Elastic Beanstalk CLI
    - `eb init`
  - Create an AWS Elastic Beanstalk environment
    - `eb create`
  - If needed, deploy your application to the AWS Elastic Beanstalk environment
    - `eb deploy`

```bash
2022-12-19 20:01:00    INFO    Instance deployment completed successfully.
2022-12-19 20:01:16    INFO    Application available at basic-express-server-dev.us-west-2.elasticbeanstalk.com.
2022-12-19 20:01:17    INFO    Successfully launched environment: basic-express-server-dev
```
