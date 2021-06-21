# Udacity Project 2 Deploy a high-availability web app using CloudFormation
This provides the cloudformation template and parameters to deploy the webapp "Udagram" for Udacity AWS Cloud DevOps Engneering project 2.

## Files
### kline-project-2-cf-template.yml
CloudFormation template which builds the cloud infrastructure and application servers for the project.

### kline-project-2-cf-parameters.json
CloudFormation parameters file for kline-project-2-cf-template.yml.


## Notes
The project description seemed to imply that all of the content would be deployed by a single cloudformation template file and this is indeed what I implemented. However, given the choice I would have split up the deployment into several files, one for network infrastructure, one for the web application.

## Usage
To create the Udagram app:
```bash
$ aws cloudformation create-stack --stack-name KlineUdagram --template-body file://kline-project-2-cf-template.yml --parameters file://kline-project-2-cf-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-2
```