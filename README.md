# multi_az_wordpress
This terraform script creates:
- VPC with IG, RT, 
- Two public subnets for EC2 instances
- Two private subnets for RDS and subnet group
- SG for ELB - HTTP and HTTPS inbound
- SG for EC2 - SSH and HTTP
- SG for RDS - Port 3306 from EC2 SG
- IAM Role Policy for EC2 instances - Allow access to th shared s3 bucket
- IAM Role for EC2 instances
- IAM Instance Profile 
- S3 Bucket
- ELB
- ELB attachement (both EC2 instances in multiple AZs)
- Two EC2 instances in US-EAST-1 (az b and c)
- two bash scripts installing and configuring wordpress on EC2 instances
- Cloudfront Distribution with custom origin (ELB)
- RDS DB


Manual work to be done:
Before tf apply  - Create Key Pair and download a private key locally
after tf apply loging to wordpress install /wp-admin directory, and add S3 bucket name to the AWS plugin.



