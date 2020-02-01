# Infrastructure

## Team Information
| Name | NEU ID | Email Address |
| --- | --- | --- |
| Ravi Kiran| 001491808 | lnu.ra@husky.neu.edu |
| Veena Iyer| 001447061  | iyer.v@husky.neu.edu|

## Create subdomain for your aws accounts
`<name>.<domain.name>`
Once created, add the nameservers to your main domain.

## Create EC2 instance
To run the script use the below command
`ansible-playbook webservers.yml -e 'command=start ssh_file=<yoursshkey> vpc_region=<region> vpc_cidr_block=<cidrblock> subnet_cidr1=<cidrblock> subnet_cidr2=<cidrblock> subnet_cidr3=<cidrblock> dns_zone=`<name>.<domain.name>`

## Delete EC2 Instance
`ansible-playbook webservers.yml -e 'command=stop ssh_file=<yoursshkey> vpc_region=<region> vpc_cidr_block=<cidrblock> subnet_cidr1=<cidrblock> subnet_cidr2=<cidrblock> subnet_cidr3=<cidrblock> dns_zone=`<name>.<domain.name>`