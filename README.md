# 3-Tier-Architecture-Diagram-for-OpenCMS
Here is the architecture diagram designed for OpenCMS 

Here , we have started entire setup from Terraform-Master instance to build the 3 tier architecture.

Region : ap-southeast-1 ( Singapore )

VPC    : 10.65.0.0/16    CIDR Block

Subnet : 3

    - web public subnet : 10.65.1.0/24
    - app public subnet : 10.65.2.0/24
    - db private subnet : 10.65.3.0/24
    
Instances 4

    - WEB01 : Apache Web (Http) Server
    - APP01 : Apache Tomcat Server + OpenCMS app
    - DB01  : Mysql Server
    - Ansible-Master : To configure software on the instances.
    
NAT Gateway : To enable instances in a private subnet to connect to the internet i.e for DB01 instance.

Router      : Set of rules to route the network.

Internet 
Gateway     : Enable access to internet from VPC

