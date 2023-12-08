# project_1
aws cloud cost optimization_identifying stale resources
Identifying stale EBS SNAPSHOTS in this project
I have craeted a lambda function that identifies EBS snapshots that are no longer associated with any active ec2 instance and delete them to save on storage cost

DESCRIPTION:
the lambda function fetches all ebs snapshots owned by my aws account and also retrives a list of active ec2 instance (running and stopped)
for each snapshot,it checks if the associated volume (if exists) is not aasociated with any active instance.
if it finds a stale snapshot, it delete it,
effectively optimizing storage costs

we use lambda function inside this lambda function we write python code we use module called boto3 ,
it will talk to the aws api and will get the complete information of ebs snapshot 
we can also trigger the lambda function using cloud watch

