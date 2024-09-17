# Applied AI Specific Notes
> [!IMPORTANT]
> Before proceeding with deployment in AAIC Account, please refrence this section for the configs and value changes to be aware of.

### GitHub Token
Before proceeding, since we have a forked deployment for our custom use case, you will need a GitHub Access token for the cloudformation config, which you can get from @Nikhil-shinde-01 .

### S3 Stagging Bucket
All of the resources are deployed using cloudformation with template files hosted on S3.
Follow the steps mentioned in this section [Create a S3 Staging Bucket](./docs/Deployment/getting-started.md#step-2--create-a-s3-staging-bucket)

### Configure S3 on your local
Using your prefered method configure AWS CLI for the project, once this is done move to next step

### Upload Files to S3 Stagging Bucket
Once the AWS CLI is configured follow the steps in this section [Step 3: Staging for Deployment](./docs/Deployment/getting-started.md#step-3--staging-for-deployment)

### CloudFormation Deployment
There are two methods you can use to initiate the deployment
1. Use the link provided at the end of the above step
2. Manually configure cloudformation

> [!CAUTION]
> Make sure to provide the GitHub Access Token in the AWS Console CloudFormation configuration form under Deployment section.
> 
> Don't use long stack names, as it has been observed to be problematic, use max 15 characters.

# Retail Demo Store

The Retail Demo Store is an eCommerce reference implementation designed to showcase how AWS services can be used to build compelling shopping experiences using modern architecture and design patterns.

> [!IMPORTANT]  
> The documentation is now supported by [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) 
>
> You can read / browse directly on github [here](./docs/index.md)
>
> Alternatively you can clone the repo and run mkdocs locally to view the documentation:
>  * Install [Mkdocs](https://squidfunk.github.io/mkdocs-material/getting-started/)
>  * run `mkdocs serve` from the root of this repo

> [!NOTE]
> Jump directly to a section of the documentation:
>
> * [How to deploy an instance in your account ](./docs/Deployment/getting-started.md)
> * [Hands-on Workshops](./docs/workshops/hands-on-workshops.md)
> * [Partner Integrations](./docs/partner-integrations/partner-integrations.md)
> * [Delivering a Demo of the Retail Demo Store ](./docs/Available%20Demos/index.md)
> * [Troubleshooting - FAQs](./docs/Deployment/troubleshooting.md)


**This project is intended for educational purposes only and not for production use.**

![Retail Demo Store Home Page](./docs/assets/retaildemostore-home-devices.png)


## Build Status

![Ruff](https://github.com/aws-samples/retail-demo-store/actions/workflows/ruff.yml/badge.svg?branch=master)
![UI Build](https://github.com/aws-samples/retail-demo-store/actions/workflows/build-ui.yml/badge.svg?branch=master)

