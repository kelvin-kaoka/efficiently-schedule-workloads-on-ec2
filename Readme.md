# efficient-workload-placements-on-aws-ec2-workflows

This project contains two serverless application directories, each configured as an AWS SAM application.
The goal here is to efficienty place workloads on AWS EC2 for processing as a result we significantly save on compute costs:
1. Utilizing AWS EC2 as ephemeral workers.
2. Efficiently scheduling workloads to existing compute.

Blog: 

## Project overview

Each subdirectory contains its own SAM template, source code, and configuration needed to package and deploy a distinct compute service.
I have included event.json for local testing.

IMPORTANT:
 - The code wont work as is; update the template, event.json and samconfig parameters for the commented items.

## Prerequisites

Before running SAM commands, make sure you have:

- AWS CLI installed and configured
- AWS SAM CLI installed
- An AWS account and credentials configured via `aws configure`
Important: Update the profile name in the global samconfig.
- Optionally Docker installed, for AWS Lambda image deployments.

## Working with the subdirectories

Important: After changing into each subdirectory, run the following commands from that directory:

### 1) Build

```bash
sam build
```

### 2) Validate

```bash
sam validate
```

### 3) Deploy

```bash
sam deploy --lint
```