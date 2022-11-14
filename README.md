# AWS-LAMBDA-FUNCTION

## Code For function lambda

```py
#we import the liberia to use aws services
import boto3
#We introduce the name of our region
region = '<REPLACE_WITH_REGION>'
#We introduce the id of our instance
instances = ['<REPLACE_WITH_INSTANCE_ID>']
#We use the EC2 service
ec2 = boto3.client('ec2', region_name=region)
#We create the function that stops our instance
def lambda_handler(event, context):
    ec2.stop_instances(InstanceIds=instances)
    print('stopped your instances: ' + str(instances))
```
