# Amazon S3 Event Notifications with Amazon EventBridge

This template will create the following resources: 
- An Amazon S3 bucket configured to publish event notifications to Amazon EventBridge
- An Amazon EventBridge Rule that checks for S3 event notifications (all events*) and triggers an Amazon SNS topic 
- An Amazon SNS Topic that will send notifications to an email address

This solution is based on the blog: https://aws.amazon.com/blogs/aws/new-use-amazon-s3-event-notifications-with-amazon-eventbridge/

## Note:
*Currently, the following S3 events are supported:
- Object Access Tier Changed
- Object ACL Updated
- Object Created
- Object Deleted
- Object Restore Completed
- Object Restore Expired
- Object Restore Initiated
- Object Storage Class Changed
- Object Tags Added
- Object Tags Deleted

## How to use:
- Create a CloudFormation stack using the `yaml` template
- In the CloudFormation parameters section, input an email address that will subscribe to the SNS Topic
- After the stack is created, confirm the subscription of the email address to the SNS topic
- To test the solution, upload any file to the S3 bucket