# Ansible

> This projets uses Ansible and AWS to deploy a site in a VPC with a private subnet, public subnet, 
> NAT gateway, jumpbox in the public subnet, RDS, elb and a server in the private subnet

Using Ansible 2.2 (boto 3 required)

Run with this command:
```sh
ansible-playbook -i hosts site.yml -e "envParam=Prod prefix=clubTandem"
``` 

### Info
AWS Regions:
* Code	---	Name
* us-east-1	--- US East (N. Virginia)
* us-west-2	---	US West (Oregon)
* us-west-1	---	US West (N. California)
* eu-west-1 --- EU (Ireland)
* eu-central-1 --- EU (Frankfurt)
* ap-southeast-1 --- Asia Pacific (Singapore)
* ap-northeast-1 ---	Asia Pacific (Tokyo)
* ap-southeast-2 ---	Asia Pacific (Sydney)
* ap-northeast-2 ---	Asia Pacific (Seoul)
* sa-east-1	--- South America (São Paulo)

Command to describe availability zones: 
```sh
aws ec2 describe-availability-zones --region us-east-1
``` 

Availability zones for us-east-1:
* us-east-1a
* us-east-1b
* us-east-1c
* us-east-1e