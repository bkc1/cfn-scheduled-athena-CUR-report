# Scheduled AWS Cost & Usage Athena reports

## Overview

This CloudFormation(CFN) stack deploys a Lambda function that calls the Athena `StartQueryExecution` API to execute a SQL query against CUR data in S3 using Athena. The report is outputted as a CSV file to a user-defined S3 output location. The Eventbridge service triggers the Lambda function on a schedule to automatically generate a fresh report.  The SQL statement can be easily modified to provide insights on a wide array of resource-level AWS billing info.

## Prereqs & Dependencies

The CFN stack for the (AWS Supported) CUR/Athena configuration in the link below must be deployed as a prereq. The Athena database and table generated by this CFN stack are intended to be used as input parameters for this project. 

* https://docs.aws.amazon.com/cur/latest/userguide/use-athena-cf.html
