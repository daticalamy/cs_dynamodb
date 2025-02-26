DynamoDB Documentation
https://docs.liquibase.com/start/tutorials/amazon-dynamodb-pro/amazon-dynamodb.html

Basic Steps:

1) Ensure Liquibase Pro key is specified, eg. use env variable LIQUIBASE_LICENSE_KEY

2) Place the below .jar in liquibase/lib folder

2a) If you are using Liquibase 4.31.0+ there is an AWS Extension that includes DynamoDB:
https://mvnrepository.com/artifact/org.liquibase.ext/liquibase-aws-extension

2b) If you are using a version prior to Liquibase 4.31.0 you'll want to download the DynamoDB Extension:
https://mvnrepository.com/artifact/org.liquibase.ext/liquibase-commercial-dynamodb

3) Make sure the following AWS keys are set:
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_SESSION_TOKEN (optional)

4) Required Permissions can be found at https://docs.liquibase.com/start/tutorials/amazon-dynamodb-pro/amazon-dynamodb.html

