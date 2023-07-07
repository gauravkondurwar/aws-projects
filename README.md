# aws-Lambda-projects(auto-stop-start-ec2)
Project: How do I stop and start Amazon EC2 instances at regular intervals using Lambda :
Description :
In your IT real-time world, we may need to schedule the EC2 instance or RDS instance to restart at regular intervals; it all depends on the needs of your project (it could be hourly, daily, weekly, or monthly). We have multiple ways to do this job.
For instance, we can use the corn jobs (Linux) or schedule tasks" (Windows) to run the script. and yet another method for performing a manual restart.
However, in AWS, we have a serverless service to handle this task which is LAMBDA.
Synopsis:
Scenario 1: I want to reduce my Amazon Elastic Compute Cloud (Amazon EC2) usage by stopping and starting my EC2 instances automatically.
Scenario 2: Create an IAM policy and execution role for your Lambda function
Scenario 3: Create Lambda functions that stop and start your EC2 instances
Scenario 3: Create Lambda functions that stop and start your EC2 instances
Scenario 4: Check the status of your EC2 instances
Scenario 5: Create EventBridge rules that run your Lambda functions



Short description
You can use AWS Lambda and Amazon EventBridge to automatically stop and start EC2 instances.
To use Lambda to stop and start EC2 instances at regular intervals, complete the following steps:

To use Lambda to stop and start EC2 instances at regular intervals, complete the following steps:
1.    Create a custom AWS Identity and Access Management (IAM) policy and execution role for your Lambda function.
2.    Create Lambda functions that stop and start your EC2 instances.
3.    Test your Lambda functions.
4.    Create EventBridge rules that run your function on a schedule.




Step 1: Open AWS Console and create one EC2 Instance.
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/79d21c07-f33b-44ec-b4bb-35a3d9e9dd71)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/9bdefd4b-92f8-46a5-bfc3-0da0b066b642)




 

 

 

 

 

 

 

 

 

 

Step 2: Create an IAM policy and execution role for  Lambda function
1:    Create an IAM policy using the JSON policy editor
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/5cf8e565-e5e4-494c-bc16-219e5e0112f3)




 

 

 

 

 

 

2: Create an IAM role for Lambda.
     Attach a permissions policy to Lambda,  choose the IAM policy that  just created.
     ![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/f313aa60-8d85-4eb4-b869-8ef2772b7b62)
     ![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/bfcc49f3-0ab2-47ed-8d85-3dc5cb53d6c4)



 

 

 

 

 

 

 

 

 

 

Step 3:  Create Lambda functions that stop and start EC2 instances
1.    Open the Lambda console, and then choose Create function.
2.    Choose Author from scratch.
3.    Under Basic information, add the following information:
For Function names, enter a name that identifies it as the function that's used to stop & Start EC2 instances. “StopEC2Instances” & “StopEC2Instances” .
For Runtime, I have chosen  Python 3.9.
Under Permissions, expand Change default execution role.
Under Execution role, choose Use an existing role.
Under Existing role, choose the IAM role that created.
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/10da704c-6b29-4462-a848-36778038d18f)


 

 

 

 

 

Step 4: Under code edit code source to stop EC2 instances.
1: Choose Deploy.
2: configure test event
3: On the Configuration tab, choose General configuration, Edit. Set Timeout to 10 seconds, and then choose Save and Test
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/9260e437-8322-4488-bd8b-27de58169c7a)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/a0a099a0-a7b5-4fc8-9846-8f0f93abac4a)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/42a540d9-bdf8-4f75-8856-847d0a65a808)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/0d0dcb4e-cb26-472b-9be0-b88fd9f01a70)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/5376cd77-ddf1-42b1-bd5c-5df2075812be)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/d60993fd-7aa3-4259-b695-8d36a600f498)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/6f8f7daf-bf0b-46de-a46c-a5802063b20c)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/c199155d-f8e8-400c-ae9f-3327026af99d)







 

 

 

 

 

 

 

 

Step 5: now I  can check the status of EC2 instances before and after testing to confirm that functions work as expected.
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/505cf3bb-631f-4bfd-a76b-6cac4fd5c14e)


 





1: functions worked Instance Stopped.
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/ccc4c94e-4607-4e47-8175-49208c4f3113)

 

2: Now Create function to start instance ( same as step 4&5 )
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/cb4b9034-527e-413e-b849-70a169c53048)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/7b82025a-cc99-4bb8-923e-68489149b43c)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/943f97dc-5f32-46bc-b133-3fb724c2e751)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/fcc24f16-5404-401e-b345-b1c9ad991d4e)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/07822120-a988-4ee7-a993-3118b48aeeae)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/eb2be19f-533c-4633-9705-439f0b5e1196)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/5cf7ab50-356e-40e3-8e5d-8c7c824f5a4e)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/34e0f1c7-a995-46c1-861f-e18a9465e113)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/71c248dd-135d-43d1-a042-fb45ea8686db)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/f42f4701-79a4-48bf-8baa-049060f298a9)












 

 

 

 

 

 

 

 

 

 

3: functions worked Instance Running.
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/985fd028-0aa1-4ea4-aadd-fc321b08c6d2)


 





Step 5: I can check  the logs in view logs.
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/651e6c4b-8cce-49f3-8bac-b207131d78d1)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/fdfe0462-047b-4df7-9c88-6be2291419dc)



 

 





Step 6: Create EventBridge rules that run Lambda functions:
1.    Open the EventBridge console.
2.    Select Create rule.
3.    Enter a Name for rule, such as "StopEC2Instances". (Optional) Enter a description for the rule in Description.
4.    For Rule type, choose Schedule, and then choose Continue in EventBridge Scheduler.
5.    For Schedule pattern, choose Recurring schedule. following steps:
Under Schedule pattern, for Occurrence, choose Recurring schedule. Then complete following steps:
Schedule type is Cron-based schedule, for Cron expression, enter an expression that tells Lambda when to stop instance. For information on expression syntax, see Schedule expressions for rules.
Cron expressions are evaluated in UTC, so adjust the expression for preferred time zone.
6.    In Select targets, choose Lambda function from the Target dropdown list.
7.    For Function, choose the function that stops EC2 instances.
8.    Choose Skip to review and create, and then choose Create.
  ![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/c0ca1f57-2cdf-452a-8255-5ed2d1954f89)
  ![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/deaa5309-db7e-4eee-be59-c3adfffdd585)
  ![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/be93ca35-25de-4a84-8f65-8172066beaa5)
  ![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/1181afe0-077d-426a-94c7-7878a4e7005e)
  ![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/5287e1cc-68bf-4fab-bc73-aa2cbbcb5f6e)
  ![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/fc9977e1-a65c-4a9d-a988-55d7da4e2f98)
  ![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/7aa1652b-4a24-46fe-a53c-5affec58a98d)
  ![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/8ddbcdf2-d824-4c70-9cd0-e3681d2e9013)








 

 

 

 

 

 

 

 

Cron-based Scheduled Expression worked instance Stopped
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/77cd271a-9ab5-401a-b35d-bf9107b4156f)


 





Step 7:  Repeat steps 1-8 to create a rule to start EC2 instances.  following steps:
Enter a name for rule, such as "StartEC2Instances".
(Optional) In Description, enter a description for rule.
In step 5, for Cron expression, enter an expression that tells Lambda when to start instances.
In step 7, for Function, choose the function that starts your EC2 instances.
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/c3f0cde6-bb0e-4436-9afb-278bb956a718)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/f1e0811f-6f9e-4f3b-b3bc-d15a7ea77f1b)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/a634679f-6a3b-423f-8423-9f9aead6d3bd)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/82d15e66-013c-4d05-9206-fb5d15884497)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/5674222c-4037-434e-9cc3-54200134500a)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/dce50823-78b0-4312-9594-6ab8ede49047)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/ed4915e1-926d-437a-997a-2663a71e164d)
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/eb8dd6fb-b4b2-4247-b86c-ab07ceb23d62)







 

 

 

 

 

 

 

 








Cron-based Scheduled Expression worked instance Running.
![image](https://github.com/gauravkondurwar/aws-projects/assets/135307780/d876ab82-b508-4e1e-a78f-950a33f94a7e)


 

we can create schedule expression rule using UTC time zone like date, time (minutes, hours), day of month, weeks, years but i have used small pacific time zone like 9:22 AM & 9:35 AM to stop and start ec2-instances for self-practice & show to how Event-Bridge rule works in this Project.
























