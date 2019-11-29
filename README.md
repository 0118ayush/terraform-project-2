Overview
This usecase covers HashiCorp's Terraform and AWS.

As a reminder, Terraform is an Infrastructure as Code tool. In other word, once the desired state of the infrastructure has been defined in a terraform file, TF will apply it to the cloud.

Usecase
You need to build a classic AWS infrastructure with Terraform, in no particular order :

1. AWS VPC, Subnet, Internet gateway
2. A load balancer
3. Three EC2 instances, that you would have provisioned with a simple webserver (apache ?)
4. Those machine should be in the VPC/subnet created beforehand
5. Those machine need to be reachable via the load balancer.
6. Configure Terraform to use Consul as a Remote state.
7. Try to use this state from a different machine, to confirm.

A typical file structure would look like this :

usecase-terraform
aws.tf
instances.tf
outputs.tf
variables.tf
terraform.tfvars

Feel free to use community modules if you believe they will make it easier for you to deliver the usecase.
