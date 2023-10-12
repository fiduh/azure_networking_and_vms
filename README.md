# Azure Networking and Virtual Machines running web servers
Azure virtual networking end-to-end and virtual machines

![VNet and VM architecture on Azure](./assets/web-server-rsg.png)


### Create a Resource Group
> Logical grouping of resources provisioned in Azure (allows for management and deletion of multiple resources at the same time)

![Create Resource Group](./assets/resource-group.png)

create-vnet.png
### Create a Virtual Network (VNET)
Emulation of physical networking and a logically isolated section in Azure, VNets can be further Segmented using Subnets and protected using NSG

![Create VNet](./assets/create-vnet.png)

### Create Subnet
Create two subnets; one public subnet for the Application Gateway and one private subnet for the webserver virtual machine 

![Create Subnets](./assets/subnets.png)


### Create a Network Security Group (NSG)
Used for network filtering at the subnet level and VM level, acts as a gatekeeper for Subnets, Defines who can connect in and out of subnet
Create a Public SG and associate it with the Public Subnet, allowing all HTTP/S traffic on ports 443/80 into the subnet and then create another Private SG, associate it with the Private Subnet, Blocking all traffic from the internet.

### Create an Application Gateway
Traffic distribution for HTTP (web) traffic (Layer 7), offering various traffic routing rules and SSL termination.
This should be created in a Subset that allows for public traffic.

### Create a Virtual Machine (VM)
A public IP address shouldn't be assigned to it, This should be in a private subnet without internet access. Only the Application gateway should be allowed to have access to it. 


