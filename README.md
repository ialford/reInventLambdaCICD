# Lambda CICD 

git clone https://github.com/nvashish123/reInventLambdaCICD.git

```bash
sam package  --output-template-file packaged.yaml  --s3-bucket vashi-lambda-code
```


```bash
sam deploy --template-file packaged.yaml --stack-name LambdaCICD --capabilities CAPABILITY_IAM
```


Create CodeBuild and code pipeline from console - 

create a IAM role for CloudFormation - follow instructions here - https://docs.aws.amazon.com/lambda/latest/dg/build-pipeline.html#with-pipeline-create-cfn-role 

Start doing controlled deployments by adding the Lambda alias and preTrafficHook


