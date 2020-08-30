# serverless-whatsapp-notifier

A WhatsApp Notification Service Using AWS Lambda and the Serverless Framework

## Environment

* Node.js >= `12.x` & npm >= `6.x`
* Serverless >= `1.80.x`
* AWS CLI >= `2.x

```
matthewwoop $ aws --version
aws-cli/2.0.40 Python/3.7.4 Darwin/19.6.0 exe/x86_64

matthewwoop $ node --version
v14.5.0

matthewwoop $ npm --version
6.14.8

matthewwoop $ serverless --version
Framework Core: 1.80.0
Plugin: 3.8.1
SDK: 2.3.1
Components: 2.34.9
```

## Serverless Configuration Check

After creating desired roles, the [hello](https://www.serverless.com/framework/docs/providers/aws/examples/hello-world/node/) serverless quick-start returning the following ensures the framework is up & running as expected.

```
matthewwoop helloWorld $ serverless invoke -f hello | jq
{
  "statusCode": 200,
  "body": "{\n  \"message\": \"Go Serverless v1.0! Your function executed successfully!\",\n  \"input\": {}\n}"
}
```

Note we specify the IAM profile a given project directory's `serverless.yml` config file.

```
service: helloworld
provider:
  name: aws
  runtime: nodejs12.x
  profile: iam-whoiam-dealwithit

...
```
