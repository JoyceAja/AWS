# Week 1

## Vocabulary
<p>AWS Availability Zone (AZ)</p>
<p>AWS Region</p>
<p>Amazon Elastic Compute Cloud(EC)</p>
<p>Amazon Virtual Private Cloud (VPC)</p>
<p>CloudFormation</p>
<p>EC2 Metadata</p>


## Getting started on AWS
1. Create free aws account
2. Add payment plan
3. Phone Verification
4. Select support plan

## Launching Amazon EC
1. Open EC2 dashboard and launch instance
2. Choose Amazon Machine Image (AMI)
3. Choose an Instance Type
4. Configure Instance Details
5. Add Storage
6. Add Tag (key & value)
7. Configure Security Group
8. Launch Instances
9. Create key pair

## Test sample app
1. Once the instance passed the status checks, select instance and copy the IPv4 Public IP
2. Open a browser and type the public IP of the Amazon EC2 instance

## Terminating the Amazon EC instance
1. On the dashboard Actions
2. Instance State
3. Terminate

## Launch an AWS CloudFormation template
1. Open CloudFormation dashboard
2. Create Stack
3. Choose template file (will get into more details creating one later on)
4. Add Stack name
5. Options page (we are going to skip for now)
6. Create

When you go back to the VPC dashboard, in Your VPCs you will see the stack you just created. Make sure to copy the vpc-id. 
Next click on Subnets, you will see four subnets. Copy the subnet-id for public a (will clarify if there is a significance 
to which on subnet is used, in regards to subnet-a or subnet-b).

You can now launch your EC2 instance. For the Network VPC paste the choose the name of the stack you created when launching
the CloudFormation. The Subnet should be subnet-public-a.

## Connecting to Amazon EC2 Instance
<p>PATH-TO-PEM-FILE with a reference to the .pem file downloaded after launching the instance</p>
<p>PUBLIC-IP with the IPv4 Public IP of the instance</p>
``` bash
chmod 400 PATH-TO-PEM-FILE 
ssh -i PATH-TO-PEM-FILE ec2-user@PUBLIC-IP 
```
