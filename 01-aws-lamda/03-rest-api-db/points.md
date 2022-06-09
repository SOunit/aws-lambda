# points

- advantage

  - no need to manage server
  - horizontal scale
  - never pay for idle
  - more reliable

- REST API structure

  - client - API gateway - Lambda - IAM Role - DynamoDB

- create DynamoDB table

  - search DynamoDB
  - create table
  - put table name, partition key
  - put create

- create Lambda function

  - set function name: serverless-api
  - execution rule: Create a new role from AWS policy templates
  - role name: serverless-api-role
  - click configure / permission / serverless-api-role

- edit role

  - why add policy?
    - to write cloud watch for a log
    - to access DynamoDB
  - how to add policy?
    - click `add permission` / `attach policy` in role page
    - search by `cloudwatchlog` and click `CloudWatchLogsFullAccess`
    - search by `dynamodb` and click `AmazonDynamoDBFullAccess`

- create API gateway
  - click `create API`
  - select `REST API`
  - add resource, check `Enable API Gateway Cors`, create resource
  - add method
  - check `Use Lambda Proxy integration`
    - to add config to request automatically?
