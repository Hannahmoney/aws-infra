# AWS VPC + ALB + AutoScaling + Endpoints (CloudFormation)
This repository contains a complete AWS infrastructure stack built with CloudFormation.
It deploys:

- 1 VPC (172.16.0.0/16)
- 2 Public subnets + 2 Private subnets
- Internet Gateway + NAT Gateway
- Application Load Balancer
- Auto Scaling Group + Launch Template
- Security Groups (ALB + EC2 + VPC Endpoints)
- S3 Bucket
- VPC Endpoints (S3 Gateway, SSM, SSMMessages, EC2Messages, CloudWatch Logs)


## Architecture

![Infrastructure Diagram](diagrams/arc.jpeg
)

### Create the stack

```bash
aws cloudformation create-stack \
  --stack-name aws-infra \
  --region us-east-1 \
  --template-body file://main.yaml \
  --capabilities CAPABILITY_IAM
```
