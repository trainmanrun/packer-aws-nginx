# packer-aws-nginx

Followed the instructions on https://learn.hashicorp.com/collections/packer/aws-get-started to create the nginx image in AWS

## How to use
1. Clone the Repo
```
git clone https://github.com/trainmanrun/packer-aws-nginx.git
cd packer-aws-nginx
```
2. Validate and Build
```
packer validate .
packer build aws-nginx.pkr.hcl
```
This will make the AMI available under the [AWS AMI management|https://ap-southeast-2.console.aws.amazon.com/ec2/v2/home?region=ap-southeast-2#Images:visibility=owned-by-me;sort=name] page. Note that as a pre-requisite, you should've already provided your AWS credentials prior to the packer build command.
```
export AWS_ACCESS_KEY_ID=YOUR_ACCESS_KEY
export AWS_SECRET_ACCESS_KEY=YOUR_SECRET_KEY
```