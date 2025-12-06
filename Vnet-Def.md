##1. What is a VNet?

Definition:
A Virtual Network (VNet) is a logically isolated network in Azure where you can deploy your Azure resources like VMs, databases, and web apps. It’s like your own private network in the cloud.

Purpose:

Provides isolation and segmentation.

Enables secure communication between Azure resources.

Supports hybrid connections with on-premises networks.

Example:
You can create a VNet VNet1 with an address space 10.0.0.0/16 to host multiple VMs and Azure services that need to communicate privately.

##2. What are Subnets, and Why do we need them?

Definition:
A Subnet is a range of IP addresses within a VNet. It helps divide the network into smaller, manageable segments.

Purpose:

Organizes resources logically.

Implements security boundaries with NSGs.

Efficient IP address management.

Example:
In VNet1 (10.0.0.0/16):

Subnet1: 10.0.1.0/24 for web servers

Subnet2: 10.0.2.0/24 for database servers

##3. What is Network Security Group (NSG)? When do you use it?

Definition:
A Network Security Group (NSG) is a firewall that controls inbound and outbound traffic to resources in a subnet or network interface.

Purpose:

Restricts unauthorized access.

Applies rules at subnet or VM level.

When to use NSG:

When you want to allow only specific traffic (like HTTP/HTTPS to web servers).

To block unwanted inbound or outbound connections.

Example:
NSG WebNSG allows inbound 80/443 and denies all other inbound traffic for a web server subnet.

##4. What is Application Security Group (ASG)? When do you prefer ASG?

Definition:
An Application Security Group (ASG) allows grouping of VMs with similar workloads to simplify NSG rules.

Purpose:

Makes NSG rules dynamic and easier to manage.

Allows you to apply security policies based on application role rather than IP addresses.

When to use ASG:

In large deployments where VMs frequently scale or change.

When you want rules like "allow traffic from Web-ASG to DB-ASG".

Example:

Web-ASG → all web servers

DB-ASG → all database servers
NSG rule: Allow traffic from Web-ASG to DB-ASG on port 1433.

##5. What is VNet Peering?

Definition:
VNet Peering connects two VNets privately in Azure, allowing resources in each VNet to communicate without using public IPs.

Purpose:

Enables seamless cross-VNet communication.

Low latency, high bandwidth connection.

Example:
VNet VNet1 (10.0.0.0/16) peered with VNet2 (10.1.0.0/16) allows a VM in VNet1 to access a database in VNet2 privately.

##6. What is Public IP?

Definition:
A Public IP is an IP address accessible from the internet.

Purpose:

Makes Azure resources (VMs, Load Balancers, etc.) reachable from outside.

Example:
A web server VM with public IP 52.172.12.34 can be accessed from a browser.

##7. What is Private IP?

Definition:
A Private IP is an IP address used for internal communication within a VNet or between VNets.

Purpose:

Ensures internal resources communicate privately.

Not accessible directly from the internet.

Example:
VM1 in Subnet1 has private IP 10.0.1.4 and VM2 in the same VNet can access it via this IP.

##8. What are Outbound Rules?

Definition:
Outbound rules define how traffic leaves a resource, subnet, or network interface to external destinations.

Purpose:

Control which destinations a VM or subnet can connect to.

Implement security for outbound traffic.

Example:

NSG outbound rule: Allow traffic from Subnet1 to 0.0.0.0/0 on port 443 (HTTPS).

Restrict all other outbound traffic.
