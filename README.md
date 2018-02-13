AWS EMR
=======
![Launch Stack](https://cdn.rawgit.com/buildkite/cloudformation-launch-stack-button-svg/master/launch-stack.svg)](https://console.aws.amazon.com/cloudformation/home#/stacks/new?templateURL=https://raw.githubusercontent.com/nclouds/aws-emr/master/emr.yaml)

This is a small demo for getting started with AWS EMR. AWS EMR is managed Hadoop Framework with support for Apache Spark, Presto etc.,

The included Cloud Formation Template, launches an EMR stack in a new VPC and executes a small step on Apache Spark

It takes an [CSV file](https://s3-us-west-2.amazonaws.com/nclouds-emr-demo/census_la.csv) as input from S3 which had Census data with male population and female population in it.

The [pyspark script](https://s3-us-west-2.amazonaws.com/nclouds-emr-demo/demo.py) calculates the sex ratio and adds it as a new column to the CSV and uploads it to the output bucket

The output bucket must be specified while creating a stack.
