System monitoring is a process to monitor resources and performance of infrastructure

Very crucial to monitor systems 
Monitoring alone isn't sufficient - it just gives bird's eye view of our system's health - that too data not in real-time
Monitoring and we need to have Alerting in place - by which we get timely information when a monitoring service detects something unusual.
System Alerts/Alert Notifications - are machine to person communication which carry time sensitive information

Services under Monitoring & Alerting umbrella in AWS Ecosystem:
    - Cloudwatch : is a defacto monitoring service which monitors key metrics of various services within AWS like - EC2, ELB, Elastic Block store etc.
    Cloudwatch is used to collect and track metrics,
                                             collect and monitor log files,
                         and automatically react to changes in the AWS Resources
                         set alarms
                
These metrics could be - general CPU consumption or memory utilization 

CloudWatch takes care of metrics part and Altering part is covered by SNS/ SES. 

CloudWatch 

Metric - variable to monitor

Belongs to Namespace

Dimension - attribute (CPU utilization, memory etc) at max there can be 30 dimensions for a metric

Dashboard of metrics

CloudWatch custom metrics -example: memory size of an ec2 instance

We can also stream out the CloudWatch metrics :  near-real-time-delivery and low Latency ---> Amazon Kinesis Firehose --> destinations

CloudWatch Log Groups: Names representing the applications
Within log groups we'll have multiple log streams - these represent log instances/log files/containers of an application

Then we can define Log expiration policy ( never expire, 1 day to 10 years…)
Can export CloudWatch logs into different streams:
    - S3 (Batch export)
    - Kinesis data stream
    - Kinesis Data firehose
    - AWS Lambda
    - OpenSearch
Logs are encrypted by default - We can setup KMS based encryption using own keys

What kind of data goes into CloudWatch Logs - Sources:
    - SDK, CloudWatch Logs Agent(sort of now deprecated), CloudWatch Unified Agent(this is being used now)
    - Elastic Beanstalk: collect logs from application
    - ECS: from containers
    - AWS Lambda: from function logs
    - VPC Flow Logs: VPC specific logs(metadata traffic)
    - API Gateway - will send all requests made to API Gateway into CloudWatch logs
    - CloudTrail based on filter
    - Route53: log DNS queries
What if we want to query logs in CloudWatch:
We can make use of CloudWatch Logs Insights - querying capability within CloudWatch Logs - allows us to write query- specify Timeframe you want to apply your query and we get result as visualization and we can view specific log lines. 
    - Allows us to search and analyze log data stored in CloudWatch logs
    - Lot of sample queries provided in console
    - Provides purpose-built query language
    - Can query multiple logs

