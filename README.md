# Azure Networking and Virtual Machines running web servers
Azure virtual networking end-to-end and virtual machines

### Create a Resource Group
Logical grouping of resources provisioned in Azure (allows for management and deletion of multiple resources at thesame time) 

### Create a Virtual Network (VNET)
Emulation of physical networking and a logically isolated section in Azure, VNets can be further Segmented using Subnets and protected using NSG

### Create a Network Security Group (NSG)
Used for network filtering at the subnet level and VM level, acts as a gatekeeper for Subnets, Defines who can connect in and out of subnet

### Applications Security Group (ASG)
Logical grouping of VMs, to aviod manually adding their individual ip addresses to NSG rules

### Create an Application Gateway
Traffic distribution for HTTP (web) traffic (Layer 7), offering various traffic routing rules and SSL termination.


