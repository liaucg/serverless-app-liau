# My First Serverless App


# Installation

Install `serverless` module via NPM:
```
$ npm install -g serverless
```

# Creating A Service

To create the project (known as a Serverless Framework "Service"), run the `serverless` command below, then follow the prompts.
```
$ serverless

Creating a new serverless project

? What do you want to make? AWS - Python - Starter
? What do you want to call this project? serverless-app-liau

✔ Project successfully created in serverless-app-liau folder

? Do you want to login/register to Serverless Dashboard? No

? Do you want to deploy now? No

What next?
Run these commands in the project directory:

serverless deploy    Deploy changes
serverless info      View deployed endpoints and resources
serverless invoke    Invoke deployed functions
serverless --help    Discover more commands
```

# Deploying
Run the following command to deploy the service.
```
$ cd serverless-app-liau
$ serverless deploy

Deploying serverless-app-liau to stage dev (ap-southeast-1)

✔ Service deployed to stack serverless-app-liau-dev (96s)

functions:
  hello: serverless-app-liau-dev-hello (1.9 kB)

Need a faster logging experience than CloudWatch? Try our Dev Mode in Console: run "serverless dev"
```

# Invocation

After successful deployment, you can invoke the deployed function by using the following command:

```
$ serverless invoke --function hello

{
    "statusCode": 200,
    "body": "{\"message\": \"Go Serverless v3.0! Your function executed successfully!\", \"input\": {}}"
}
```

