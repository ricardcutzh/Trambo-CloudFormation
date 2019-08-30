# vpc.yml

## Parameters
| Parameter      | Description | Type    |
| :---        |    :----:   |          ---: |
| VPCName     | Name of the VPC     |   String |
| Subnet1Name     | Name of the subnet 1    |   String |
| Subnet2Name     | Name of the subnet 2     |   String |
| Subnet3Name     | Name of the subnet 3     |   String |
| Subnet4Name     | Name of the subnet 4   |   String |
| Subnet5Name     | Name of the subnet 5     |   String |
| Subnet6Name     | Name of the subnet 6     |   String |
| CIDRBlock     | address block for the VPC   |   String |
| NetworkMask     | Subnetmask to be used for the VPC    |   String |

## Resources
### VPC
* Block address for the VPC: 192.168.0.0/24 

### Subnet 1 (Public)
* Address Block: 192.168.0.0/27
* Availability Zone: us-west-2a
* Automatic public IP assigment

### Subnet 2 (Public)
* Address Block: 192.168.0.32/27
* Availability Zone: us-west-2a
* Automatic public IP assigment

### Subnet 3 (Public)
* Address Block: 192.168.0.94/27
* Availability Zone: us-west-2a
* Automatic public IP assigment

### Subnet 4 (Private)
* Address Block: 192.168.0.126/27
* Availability Zone: us-west-2b
* No Automatic public IP assigment

### Subnet 5 (Private)
* Address Block: 192.168.0.158/27
* Availability Zone: us-west-2b
* No Automatic public IP assigment

### Subnet 6 (Private)
* Address Block: 192.168.0.190/27
* Availability Zone: us-west-2b
* No Automatic public IP assigment

### Internet Gateway
* Internet Gateway that will be used for the VPC

### Internet Gateway Attachment
* Resource used to attach the internet gateway to the vpc

### Public Route Table
* Resource to define a route table that will be used by the public subnets

### Internet Route
* Resource that defines the exit to internet in the public subnets

### Public Subnets association
* This resources are used to associate public subnets to the Public Route Table

### Private Route Table
* Resource that defines the route table that will be used by the public subnets

### Private Subnets association
* This resources are used to associate private subnets to the Privat Route Table

### VPC's Security Group Definition
* Defines the inbound rules for the vpc

## Outputs
* VPC: Id of the created VPC
* SubnetPublic1: id of the public subnet 1
* SubnetPublic2: Id of the public subnet 2
* SubnetPublic3: Id of the public subnet 3