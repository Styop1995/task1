## SIA Application Documentation.

* IaC: Terrafom.  
* CI/CD: GitHub Action.
* Frontend: The user interface for the application, hosted on Amazon S3 and distributed through CloudFront.
* Backend: The server-side logic and API endpoints, implemented using AWS Lambda functions.
* Authentication: User authentication and authorization handled by AWS Cognito.
* Database: A relational database managed by Amazon RDS for storing application data.
* File Storage: Amazon S3 used for storing files uploaded by users.
* Caching: ElastiCache used as an in-memory data store for caching frequently accessed data.



## The Pipeline Sections and steps

# For running the Pipeline as a variable Set access key and Secret key in GitHub Action. 

The following steps are included in the Pipeline:
* Checkout code 
* Install Terraform
* Configure AWS Credentials
* Initialize Terraform `Terraform init`
* plan Terraform `terraform plan --auto-approve`


## 