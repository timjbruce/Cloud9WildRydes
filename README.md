# Cloud9WildRydes
Setup of Cloud9 for WildRydes

Integrate and Use Cloud9 for WildRydes

## 1) Create the CodeCommit Repo
### a) In the console, select CodeCommit 
### b) Click on "Create Repository" 
### c) Name it "WildRydesWebsite" 
### d) Skip Email notification 
### e) use connection type https


## 2) Setup your Cloud9 Instance
### a) In the console, select Cloud9
### b) Click Create Environment 
### c) Name it "WildRydes" 
### d) Leave the defaults and click Next Step 
### e) Click "Create Environment" 
### f) When the environment is up, check for git by typing "git --version" 
#### 1) if you do not have git, type "sudo yum update" 
#### 2) "sudo yum install git" 
#### 3) check for git by typing "git --version" 
### g) Check for the AWS CLI by typing "aws --version" 
#### 1) if you do not have aws cli, install it by typing "sudo yum install aws-cli" 
### h) type "git config --global credential.helper '!aws codecommit credential-helper $@'" 
### i) type "git config --global credential.UseHttpPath true"
### j) type "mkdir WildRydesWebsite"
### k) type "cd WildRydesWebsite" 
### l) type "aws s3 sync s3://wildrydes-us-east-1/WebApplication/1_StaticWebHosting/website . --region us-east-1"
### m) type "git init ."
### m) type "git add ."
### n) type "git commit . -m "Initial Commit""
### o) type "git remote add origin https://git-codecommit.us-east-1.amazonaws.com/v1/repos/WildRydesWebsite"
### p) type "git push -u origin master"
