Identity based policy - can be applied to users/groups/roles
Resource based policy - can be applied to resources (bucket policy/instancepolicy)


cd .~/aws --> at this location we have config and credentials - we can check cat credentials and get the aws access key and secret key

AWS Security Token Service:

provides short lived or temporary credentials

Instance profile --> IAM role --> attempts to assume role --> 


Trust Policy (who can assume the role - is also an example of resource based policy) & Permissions Policy (allowed or denied to a specific entity - is an identity based policy.)

Temporary credentials are used with Identity Federation, delegation, cross-account access, and IAM roles.


IAM Access Control:

Identity Based Policies (JSON permission policy that control what actions an identity can perform on which resources, and under what conditions) & 

Inline policy - have one-to-one relationship with user/role/group
i.e. we can't share or use the inline policy for other roles/group/user

Managed policy - can be either AWS Managed or Customer Managed policy
- can attach managed policy to multiple entities(user/groups/roles)


Resource Based Policies (JSON policy documents that you can attach to a resource such as an Amazon S3 bucket)

- resource-based policies grant the specified principal permission to perform specific actions on the resource


Access Control Methods - RBAC & ABAC:
### Autoscaling Accelerates Application Availability and Access Always Add Automation As An Appropriate Action And Approach Anywhere Autoscaling Acts As An Advantage

