# AWS-CI-CD-Project
Set up CI/CD pipeline on AWS

AWS Services used:
1. AWS BeanStalk
2. AWS RDS
3. S3
4. AWS CodeCommit
5. AWS CodeBuild

STEPS TAKEN:-
- -> Log to AWS Account
- -> Create Key-pair
- -> Create Elastic Beanstalk Environment
- -> Create RDS
- -> Allow port 3306 in RDS SG from Beanstalk SG
- -> Initialize database
     - SSH to Beanstalk
     - Install mysql client and login to RDS
     - Deploy db_backup.sql file
- -> Update health check to /login in Target Group
- -> Build and Deploy artifact to Beanstalk
- -> Create CodeCommit Repo
- -> Clone the Git repo to CodeCommit Repo
- -> Configure CodeBuild
- -> Edit Build Commands and replace it with the commands in buildspec file(remember to update the commands)
- -> Start the build
- -> Configure CopePipeline
- -> Test the URL
