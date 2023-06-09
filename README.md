## SIA Application Documentation.

* IaC: Terrafom.  
* CI/CD: GitHub Action.
* Frontend: The user interface for the application, hosted on Amazon S3 and distributed through CloudFront.
* Backend: The server-side logic and API endpoints, implemented using AWS Lambda functions.
* Authentication: User authentication and authorization handled by AWS Cognito.
* Database: A relational database managed by Amazon RDS for storing application data.
* File Storage: Amazon S3 used for storing files uploaded by users.
* Caching: ElastiCache used as an in-memory data store for caching frequently accessed data.


## Providers

| Name | Version |
|------|---------|
| aws | n/a |



## The Pipeline Sections and steps

For running the Pipeline as a variable Set access key and Secret key in GitHub Action. 
The following steps are included in the Pipeline:
* Checkout code 
* Install Terraform
* Configure AWS Credentials
* Initialize Terraform `Terraform init`
* plan Terraform `terraform plan --auto-approve`


## Use the following list of the variables which is necessary to run the task

## Inputs

| Name                | Description                                                                                                 | Type     | Default       | Required |
|---------------------|-------------------------------------------------------------------------------------------------------------|----------|---------------|:-----:|
| asg\_config         | Map configuration for auto scaling groups                                                                   | `map`    | n/a           | yes |
| environment         | Tag to assign to EC2 instances launched by this ASG                                                         | `string` | n/a           | yes |
| project\_name       | Project name. Used for tagging resources                                                                    | `string` | n/a           | yes |
| asg\_shutdown\_hook | Map configuration for auto scaling groups' shutdown hooks                                                   | `map`    | `{}`          | no |
| aws\_region         | AWS region to use for project                                                                               | `string` | `"eu-west-1"` | no |
| enable              | Enable or dis2able creation of module                                                                       | `bool`   | `true`        | no |
| tags                | Additional tags to be propagated on EC2 (Should be set in order to comply with Railsr tagging requirements) | `map`    | `{}`          | no |
