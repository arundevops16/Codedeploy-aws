

Assignment: Launch EC2 instance using CLI install java, jenkins, and tomcat in ec2 instance using ansible roles and setup sprig3hibernate job in jenkins and uasing aws code deploy and jenkins deploy war file into tomcat.

Using CLI launch an ec2 instance

Installed code deploy agent on ec2 instance.

Attached a role ec2 to access code deploy and s3 bucket.

Created an ansible role to install java, jenkins, and tomcat.

Using aws code deploy created an deployment application.

Attached an IAM service role which allows the code deploy service to access ec2.

Installed aws code deploy plugin in jenkins.

created a job in jenkins and configured to deploy SpringHibernate application in apache tomcat.

![codedeploy](https://github.com/arunkundrupu1990/BuddyAssignments/blob/master/codedeploy/images/01%20spring%20aws%20CD%20jenkins.png)

![codedeploy](https://github.com/arunkundrupu1990/BuddyAssignments/blob/master/codedeploy/images/02%20spring%20aws%20CD%20jenkins.png)

Created s3 bucket in aws.

Installed s3 publisher plugin to upload files to s3 bucket

Under post build actions

1. selected the publish artifacts to s3 bucket and configured.

![codedeploy](https://github.com/arunkundrupu1990/BuddyAssignments/blob/master/codedeploy/images/03%20spring%20aws%20CD%20jenkins.png)

2. Deploy an application to aws code deploy

![codedeploy](https://github.com/arunkundrupu1990/BuddyAssignments/blob/master/codedeploy/images/04%20spring%20aws%20CD%20jenkins.png)

Created appspec.yml file and pushed in springhibernate project in github

while deploying got an error that appsepec file is not present in

![codedeploy](https://github.com/arunkundrupu1990/BuddyAssignments/blob/master/codedeploy/images/06%20error%20code%20deploy.png)

again got error that war file is not there in code deploy agent.

![codedeploy](https://github.com/arunkundrupu1990/BuddyAssignments/blob/master/codedeploy/images/08%20code%20deploy%20error3.png)

so specified the correct path in appspec file source also in jenkins job configuration.

![codedeploy](https://github.com/arunkundrupu1990/BuddyAssignments/blob/master/codedeploy/images/05%20spring%20aws%20CD%20jenkins.png)

war file deployed successfully to tomcat server. And code deploy application revision is successful.

 ![codedeploy](https://github.com/arunkundrupu1990/BuddyAssignments/blob/master/codedeploy/images/10%20CD%20success.png)

![codedeploy](https://github.com/arunkundrupu1990/BuddyAssignments/blob/master/codedeploy/images/12%20CD%20success1.png)


