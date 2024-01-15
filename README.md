It is a demo application for voting, but this time it is redesigned to use the capabilities of AWS directly: it consists of two front-end components (JS Single-Page Application) and three back-end components ( Python).

We propose the following scheme: publish static files in S3 buckets (one for each frontend), host backends as Lambda functions and make them accessible using API Gateway. We suggest running the vote processor on EC2, although you may prefer pure serverless.
Used tech
✅ EC2
✅ S3
✅ CloudFront
✅ database (DynamoDB)
✅ VPC
✅ SQS queue
✅ SNS notifications
✅ Serverless (API Gateway, Lambda)
✅ IAM
Challenge:

⚠️ IaaC (Terraform, CloudFormation, Cloud Development Kit)
⚠️ Billing и Costs
Components
API Gateway
voting frontend, Javascript
voting backend, Python
vote processor, Python
database, DynamoDB
result backend, Python
result frontend, Javascript
Architecture
Screenshot_31

For terraform, i used serverless lambda instead of ec2

