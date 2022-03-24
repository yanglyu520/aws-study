## Lambda
What is lambda?
1. Virtual functions
2. Limited by time - short executions - ephemeral serverless computing
3. Run on-demand
4. scaling is automated

Services that can trigger Lambda:
1. User Invoked:
- Elastic Load Balancing(application load balancer)
- Amazon API Gateway
- Amazon CloudFront
- Amazon S3 Batch

2. Service Invoked
- Amazon Cognito
- AWS Step Functions

3. Other Services
- Amazon Lex
- Amazon Alexa
- Amazon Kinesis Data Firehose
- CloudWatch Events --> trigger every one hour --> cronjob in lambda

Run `deploy` and then `test` to run the lambda function

4. AWS CLI for lambda
- `aws lambda list-functions`

5. upload go binary to AWS console
- `goos build -o main main.go && zip archive.zip main`

6. Understand the lambda packages
- Inside the main function `lambda.Start(Handler)` will be the entry point to start the Handler function
- The handler function will take care of an event and give a response and has a structure like this `func HandleLambdaEvent(event MyEvent) (MyResponse, error)`


7. More on the handler
- The handler must be a function.

- The handler may take between 0 and 2 arguments. If there are two arguments, the first argument must implement context.Context.

- The handler may return between 0 and 2 arguments. If there is a single return value, it must implement error. If there are two return values, the second value must implement error. For more information on implementing error-handling information, see AWS Lambda function errors in Go.








