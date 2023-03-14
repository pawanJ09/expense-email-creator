[![Python Lint](https://github.com/pawanJ09/expense-email-creator/actions/workflows/python-lint.yml/badge.svg)](https://github.com/pawanJ09/expense-email-creator/actions/workflows/python-lint.yml)
[![AWS Lambda Package and Deploy](https://github.com/pawanJ09/expense-email-creator/actions/workflows/aws-lambda-package-deploy.yml/badge.svg)](https://github.com/pawanJ09/expense-email-creator/actions/workflows/aws-lambda-package-deploy.yml)
[![AWS Lambda Test](https://github.com/pawanJ09/expense-email-creator/actions/workflows/aws-lambda-test.yml/badge.svg)](https://github.com/pawanJ09/expense-email-creator/actions/workflows/aws-lambda-test.yml)

# Expense Email Creator

This app will create email identities in AWS SES and will be considered a registration step for 
the new user. After identity creation user will receive an email to subscribe to the events from 
AWS SES which they have to accept before the identity can be verified.

## Requirements

For building and running the application you need:

- [Python3](https://www.python.org/downloads/)

```shell
pip3 install -r requirements.txt
```
OR
```shell
pip install -r requirements.txt
```

## Running the application locally

You can run the main.py program to get started. This file has the __main__ method.

```shell
python3 ./src/main.py
```
OR
```shell
python ./src/main.py
```

## Trigger AWS Lambda with Test event from cli

```shell
aws lambda invoke --function-name expense-email-creator \
--invocation-type RequestResponse \
--payload file://events/test-agw-event.json \
--cli-binary-format raw-in-base64-out /dev/stdout
```
