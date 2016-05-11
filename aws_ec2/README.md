## AWS EC2 example

## Setup
Change line 7 in `main.yml` file to the aws VPC you want to use.
Playbook creates:

- ssh key
- security group (firewall rules)
- private DNS
- iam roles (role and policy)
- ec2 VM

If you do not wish to use private DNS (route53), VPC variable is not
needed and can be removed

Before running playbook, you will need to install and configure `boto`.

## Run
`ansible-playbook main.yml`
