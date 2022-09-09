# Continuous integration and delivery (CI/CD) using CDK Pipelines
CDK Pipelines is a construct library module for painless continuous delivery of AWS CDK applications. Whenever you check your AWS CDK app's source code in to AWS CodeCommit, GitHub, or CodeStar, CDK Pipelines can automatically build, test, and deploy your new version.

CDK Pipelines are self-updating: if you add application stages or stacks, the pipeline automatically reconfigures itself to deploy those new stages and/or stacks.

For more reading visit the [aws documentation](https://docs.aws.amazon.com/cdk/v2/guide/cdk_pipeline.html).

##Task
This is a simple demo of Cloud Development Kit pipeline usingjavascript. The goal is to identify objects/labeles on an image stored on S3 bucket via amazon Rekognition

# Steps
## 1. install the CDK
```bash
sudo npm install -g aws-cdk
```
For the purposes of this of this demo, the directory name must be cdk-app/ to go with the rest of the tutorial, changing it will cause an error

```bash
mkdir cdk-app & cd cdk-app/
```
### initialize the application
```bash
cdk init --language javascript
```
### verify it works correctly
cdk ls

### install the necessary packages
```bash
npm install @aws-cdk/aws-s3 @aws-cdk/aws-iam @aws-cdk/aws-lambda @aws-cdk/aws-lambda-event-sources @aws-cdk/aws-dynamodb
```


## 2. copy the content of /resources/cdk-app-stack.js into lib/cdk-app-stack.js


# 3. setup the Lambda function
```bash
mkdir lambda && cp ../resources/index.py lambda/
```

# 4. bootstrap the CDK application
```bash
cdk bootstrap
```

# 5. (optional) synthesize as a CloudFormation template

```bash
cdk synth
```

# 6. deploy the CDK stack

```bash
cdk deploy
```

# 7. Cleanup
 empty the s3 bucket
 destroy the stack by issuing the command `cdk destroy`

