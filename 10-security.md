# Security
* **IAM policy**: sagemaker:CreatePresignedNotebookInstanceUrl
* Have to option to grant Root access to the machine that's running the notebook instance. 
    * Might be a security risk. 
    * Can restrict the access if needed
    * Can associate a lifecycle script that runs when the notebook is started
    * Doesn't support resource based policies
* **AmazoneSageMakerFullAccess** policy: Grants admin access to SageMaker + specific access to a lot of other services such as cloud watch and logs
    * Eg. can SEE objects in S3, but can't access them

## Sagemaker and VPC
Sagemaker deploys to a public VPC by defaults
* Useful to get packages
* For security sake we might want to create a custom VPC with a private subnet and deploy it into that. We can then configure it with S3 VPC endpoint or NAT Gateway. 