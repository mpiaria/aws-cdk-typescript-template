# Welcome to your CDK TypeScript project

[![build-verify](https://github.com/mpiaria/aws-cdk-typescript-template/actions/workflows/build-verify.yml/badge.svg)](https://github.com/mpiaria/aws-cdk-typescript-template/actions/workflows/build-verify.yml)

This is a blank project for CDK development with TypeScript.

The `infrastructure/cdk.json` file tells the CDK Toolkit how to execute your app.

## Usage

1. You will need to add the GitHub OIDC provider to IAM. Check out the [Adding the Identity Provider to AWS](https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services#adding-the-identity-provider-to-aws) documentation for an explanation of how to do that.

2. The [build-verify workflow](.github/workflows/build-verify.yml) requires the following GitHub Secrets to be accessible by GitHub Actions:
   - AWS_REGION - the region to which you will deploy your CDK stack(s)
   - ROLE_TO_ASSUME - the ARN of the IAM role to be assumed when authenticating using the GitHub OIDC provider

## Useful commands

- `cdk deploy` deploy this stack to your default AWS account/region
- `cdk diff` compare deployed stack with current state
- `cdk synth` emits the synthesized CloudFormation template
- `npm run build` compile typescript to js
- `npm run clean` delete the outputs of all projects
- `npm run format-check` check if the files are formatted
- `npm run format-write` edit files in-place
- `npm run lint` statically analyze your code to find problems
- `npm run lint-fix` automatically fix problems
- `npm run test` perform the jest unit tests
- `npm run watch` watch for changes and compile
