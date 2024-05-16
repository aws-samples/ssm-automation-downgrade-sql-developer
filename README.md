## How to automate downgrading SQL Server to Developer edition on Amazon EC2

This repo hosts AWS Cloudformation template for AWS blog post: How to automate downgrading SQL Server to Developer edition on Amazon EC2 published on the [Microsoft Workloads on AWS](https://aws.amazon.com/blogs/modernizing-with-aws/) blog channel. 
we will show you how to automate the process of downgrading from Microsoft SQL Server Enterprise or Standard edition to SQL Server Developer edition to save cost.

Be sure to:

* Change the title in this README
* Edit your repository description on GitHub

## Overview
This simple solution uses a combination of [AWS CloudFormation](https://aws.amazon.com/cloudformation/) and [Automation](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-automation.html), a capability of [AWS Systems Manager (SSM)](https://aws.amazon.com/systems-manager/), to automatically deploy a duplicate of your non-production database(s) on SQL Server Developer edition. The solution runs a series of PowerShell scripts that are delivered via a SSM [Run Command](https://console.aws.amazon.com/systems-manager/run-command/) to downgrade to SQL Server Developer edition. The automation creates an Amazon Machine Image (AMI) of the existing Amazon EC2 instance and runs the scripts on a new Amazon EC2 instance launched from that AMI as shown in the solution architecture diagram:


![Solution_architecture](https://github.com/aws-samples/ssm-automation-downgrade-sql-developer/blob/main/ssm-automation-downgrade-sql-developer.png)


## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

