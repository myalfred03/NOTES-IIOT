**IIoT notes**

![alt text](<Screenshot%202024-11-10%20164531.png>)

## Roles 
*User root*  Is only for access with more privileges
We recommend make admin/dev/readonly users.

Steps: 

1. Billing and Cost Management
Account
2. IAM user and role access to Billing information  (enable)
3. Acces IAM Roles
4. Make User group
5. Define type of role in this case: AdministratorAccess
AWS managed - job function 

For best practice make a user IAM 

Admin Role

User Role

Read only role

Developers access

IAM - Security credentials  Create access key

- Command Line Interface (CLI) 
- For more security install AWS CLI in your device to access managemente console. https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html#getting-started-install-instructions 
- Command Line Interface (CLI)
You plan to use this access key to enable the AWS CLI to access your AWS account.
- Save CSV file properly.

## Make Alias
- Go to IAM 
- Select ID account
- Make a alias name
 
## Billing and Cost Management
 
 Go to: 
 - Preferences and Settings - Billing Preferences 
 - Invoice delivery preferences (enable)
 - Alert preferences Info - AWS Free Tier alerts - Delivered to - mail@gmail.com
 - CloudWatch billing alerts - Delivered

 Then Configure CloudWatch : 

-  Create alarms 
- CloudWatch  - Alarms - Create alarm