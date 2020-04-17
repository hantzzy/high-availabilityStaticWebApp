# high-availabilityStaticWebApp
deploy your static website (JavaScript and HTML) from S3 Storage and deploy to a web servers with high availability.

## This project uses 3 different cloud formation templates. With the root template being Udagram.yml

The other templates are network.yml and launchconfiguration.yml  with a parameter file in json. 

## Udagram.yml:

- Root stack 
- Deploye both network.yml and launchconfiguration.yml
- both templates are currently stored in my public AWS bucket:
  - https://hantzalvarez.s3.amazonaws.com/udagramTemplate/network.yml
  - https://hantzalvarez.s3.amazonaws.com/udagramTemplate/launchconfiguration.yml

## network.yml:

- Deploy the VPC, Pub/Priv Subnets, IGW and routing. 


## launchconfiguration.yml:

- Which implements the the projects fully, by deploying the LoadBalancer, Launch Configuration, AutoScaling group a health check, security groups and a Listener and Target Group.
- Also deploy the output of the LB DNS name.
