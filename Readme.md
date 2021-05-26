# Readme

## function structure 

Hanlder / Controller / Service

Handler interacts with Lambda, contains function configuration, no business logic

Controller processes events and implement core business logic

Service integrates with external service and provides service abstractions

## using libraries and frameworks

download and start --> bootstrap runtime --> start code 
<---- cold start       ---------------->

AWS Serverless Java Container
AWS Serverless Express (node.js)
Zappa (Python)

## Managing serverless application 

Source Control / IDE / Build / Deployment tools are the same

Serverless application framework is new. 

Author - Build -|- Package  -   Deploy 
code     app       zip      S3  Lamba function
IDE + Build Tool |  Application Framework

Deployment Steps:
1. Build
2. Zip code
3. Upload to AWS S3
4. Create/update role
5. Create function
6. Create REST API
7. Create resource
8. Create method
9. Update integration
10. Create table

We can leverage AWS SAM Template instead of CloudFormation templates

AWS SAM CLI  zip, upload, update
$ sam package
$ sam deploy

Popular frameworks:
APEX
ZAPPA
serverless
AWS SAM
SPARTA
Claudia.js
Chalice

## Source Code management

separate repo for each service, which may consists of multiple functions and dependent services

use one repo per service and template. 

## Set up development Environment

CI/CD build-\>deploy-\>test-\>deploy

Shared account or separate account

The good thing is that AWS only charges when Lambda function runs. 

## Testing and Debugging

### Local testing

automated unit tests

Mocking Options: DynamoDB local and LocalStack, custom mocks, or just don't do it.

### Remote integration test



### automated integration test 

### Debug

Use IDE debugger on the Docker container provided by SAM CLI. 

SAM CLI simulate the Lambda framework that runs locally. 




