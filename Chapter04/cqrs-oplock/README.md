# CQRS Inverse Oplock

This example includes a Lambda function to write events to a Kinesis stream and Lambda function to consume from the stream and conditionally write to a DynamoDB table.

> _Please refer to the root README for installation and general instructions._

## Steps
1. Execute: `npm install`
2. Execute: `npm run dp:dev:e`
3. In the AWS console review the various tabs for the following:
   * Cloudformation Stack: `cndp-cqrs-oplock-dev`
   * DynamoDB Tables: `dev-cndp-cqrs-oplock-view`
   * Kinesis Stream: `dev-us-east-1-cndp-cqrs-oplock-stream`
   * Lambda functions: `cndp-cqrs-oplock-dev-command` and `cndp-cqrs-oplock-dev-consumer`
4. Invoke Lambda function `cndp-cqrs-oplock-dev-command` from the AWS console by pressing the Test button.
   * Accept the defaults if asked.
5. Inspect the DynamoDB tables for the new contents
6. Inspect the Lambda Monitoring tab and logs for each function
7. Execute: `npm run rm:dev:e`
