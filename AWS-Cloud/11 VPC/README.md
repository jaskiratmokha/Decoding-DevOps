# VPC Overview

AWS Virtual Private Cloud (VPC) enables you to launch AWS resources in a logically isolated virtual network, providing you with complete control over your network configuration. Let's delve into the various components and functionalities of VPC:

## CIDR, Private vs Public IP

Understanding Classless Inter-Domain Routing (CIDR) notation and the distinction between private and public IP addresses is fundamental to VPC configuration. CIDR blocks define the IP address range for a VPC, with private IPs used for internal communication and public IPs for external communication.

## Default VPC Overview

AWS automatically creates a default VPC for each AWS account, simplifying the process of launching instances. The default VPC comes pre-configured with subnets across multiple availability zones, an internet gateway, route tables, and security groups.

## VPC Hands On

1. Access the AWS Management Console.
2. Navigate to the VPC dashboard.
3. Click on "Create VPC".
4. Enter the desired CIDR block for the VPC.
5. Configure additional settings such as DHCP options and tagging.
6. Click on "Create VPC" to create the VPC.

## Subnet Overview

Subnets partition a VPC's IP address range, allowing you to isolate resources and control traffic flow within your network. Subnets are associated with specific availability zones and can be configured as public or private.

## Subnet Hands On

1. Navigate to the VPC dashboard.
2. Click on "Create Subnet".
3. Select the VPC for the subnet.
4. Enter the desired CIDR block for the subnet.
5. Choose the availability zone for the subnet.
6. Configure additional settings such as route table association and tagging.
7. Click on "Create Subnet" to create the subnet.

## Internet Gateways & Route Tables

Internet gateways facilitate communication between instances within a VPC and the internet. Route tables define the traffic flow within the VPC, directing traffic to internet gateways or other destinations.

## Internet Gateways & Route Tables Hands On

1. Navigate to the VPC dashboard.
2. Click on "Internet Gateways".
3. Click on "Create Internet Gateway".
4. Attach the internet gateway to the VPC.
5. Navigate to the route tables.
6. Edit the route table associated with the public subnet.
7. Add a route to the internet gateway for internet-bound traffic.
8. Save the route table configuration.

## Bastion Hosts

Bastion hosts serve as an intermediary for secure access to instances within private subnets. They provide a controlled entry point for SSH or RDP access to private instances.

## Bastion Hosts Hands On

1. Launch an EC2 instance in a public subnet.
2. Configure the security group to allow SSH/RDP access from specific IP addresses.
3. Connect to the bastion host using SSH/RDP.
4. From the bastion host, connect to private instances within the VPC using their private IPs.

## NAT Instances

Network Address Translation (NAT) instances allow instances within private subnets to initiate outbound traffic to the internet while blocking inbound traffic.

## NAT Instances Hands On

1. Launch an EC2 instance in a public subnet to serve as the NAT instance.
2. Disable the source/destination check for the NAT instance.
3. Modify the route table associated with private subnets to route internet-bound traffic through the NAT instance.
4. Update the security group of the NAT instance to allow outbound traffic.

## NAT Gateways

NAT gateways provide similar functionality to NAT instances but are managed AWS resources, offering greater scalability and availability.

## NAT Gateways Hands On

1. Navigate to the VPC dashboard.
2. Click on "NAT Gateways".
3. Click on "Create NAT Gateway".
4. Select the public subnet for the NAT gateway.
5. Allocate an Elastic IP address.
6. Create or select the route table associated with private subnets.
7. Add a route to the NAT gateway for internet-bound traffic.
8. Save the route table configuration.

## NACL & Security Groups

Network Access Control Lists (NACLs) and Security Groups are essential for controlling inbound and outbound traffic at the subnet and instance level, respectively.

## NACL & Security Groups Hands On

1. Navigate to the VPC dashboard.
2. Click on "Network ACLs".
3. Create a new NACL or modify the default NACL.
4. Configure inbound and outbound rules to allow or deny traffic based on IP addresses and port ranges.
5. Click on "Save" to apply the NACL configuration.
6. Navigate to the EC2 dashboard.
7. Click on "Security Groups".
8. Create a new security group or modify an existing security group.
9. Configure inbound and outbound rules to allow or deny traffic based on IP addresses and port ranges.
10. Click on "Save" to apply the security group configuration.

## VPC Peering

VPC peering enables communication between instances in different VPCs, allowing you to extend your network architecture across multiple accounts and regions. 

## VPC Peering Hands On

1. Navigate to the VPC dashboard.
2. Click on "Peering Connections".
3. Click on "Create Peering Connection".
4. Enter the details for the peering connection, including the requester VPC and accepter VPC.
5. Review the settings and click on "Create Peering Connection".
6. Accept the peering connection in the accepter VPC.
7. Update the route tables in both VPCs to route traffic to the peering connection.

## VPC Endpoints

VPC endpoints allow private instances to securely access AWS services without traversing the internet, enhancing security and reducing latency.

## VPC Endpoints Hands On

1. Navigate to the VPC dashboard.
2. Click on "Endpoints".
3. Click on "Create Endpoint".
4. Select the VPC and service for the endpoint.
5. Configure additional settings such as security groups and policies.
6. Click on "Create Endpoint" to create the endpoint.

## VPC Flow Logs

VPC flow logs capture information about the traffic flowing through network interfaces in your VPC, facilitating troubleshooting, security analysis, and compliance monitoring.

## VPC Flow Logs Hands On + Athena

1. Navigate to the VPC dashboard.
2. Click on "Flow Logs".
3. Create a new flow log or modify an existing flow log.
4. Configure the flow log settings, including the traffic type and destination.
5. Click on "Save" to apply the flow log configuration.
6. Use Amazon Athena to query and analyze the flow log data stored in Amazon S3.

## Site to Site VPN, Virtual Private Gateway & Customer Gateway

Site-to-Site VPN connections establish secure connections between your on-premises network and your AWS VPC, extending your corporate network into the cloud.

## Site to Site VPN, Virtual Private Gateway & Customer Gateway Hands On

1. Navigate to the VPC dashboard.
2. Click on "Virtual Private Gateways".
3. Create a new virtual private gateway.
4. Attach the virtual private gateway to the VPC.
5. Configure the customer gateway on the on-premises side.
6. Create a VPN connection in the VPC dashboard.
7. Configure the VPN connection settings, including the customer gateway and routing options.
8. Download the VPN configuration file and configure the on-premises VPN device.

## Direct Connect & Direct Connect Gateway

AWS Direct Connect provides a dedicated network connection between your on-premises environment and AWS, offering consistent network performance and enhanced security.

## Direct Connect + Site to Site VPN

Combining Direct Connect with Site-to-Site VPN connections enables hybrid network architectures, providing flexibility, scalability, and redundancy.

## Transit Gateway

AWS Transit Gateway simplifies network connectivity by acting as a hub that connects multiple VPCs and on-premises networks, streamlining network management and reducing costs.

## VPC Traffic Mirroring

VPC Traffic Mirroring allows you to capture and inspect network traffic flowing through your VPC, facilitating network monitoring, troubleshooting, and security analysis.

## IPv6 for VPC

IPv6 support in VPC enables you to allocate IPv6 addresses to instances, subnets, and other resources, ensuring compatibility with IPv6-enabled networks.

## IPv6 for VPC - Hands On

1. Navigate to the VPC dashboard.
2. Enable IPv6 support for the VPC.
3. Allocate an IPv6 CIDR block for the VPC.
4. Update the subnet configurations to enable IPv6 addressing.
5. Assign IPv6 addresses to instances within the VPC.

## Egress Only Internet Gateway

Egress Only Internet Gateway enables outbound IPv6 internet access for instances within your VPC while preventing inbound traffic from the internet.

## Egress Only Internet Gateway Hands On

1. Navigate to the VPC dashboard.
2. Click on "Egress Only Internet Gateways".
3. Create a new Egress Only Internet Gateway.
4. Attach the Egress Only Internet Gateway to the VPC.
5. Update the route table associated with the subnets to route outbound IPv6 traffic through the Egress Only Internet Gateway.

## Section Cleanup

Best practices for cleaning up resources and terminating unused components within your VPC environment to optimize costs and maintain security.

## VPC Section Summary

A comprehensive summary of key concepts, configurations, and best practices covered in the VPC section, reinforcing learning objectives and providing a quick reference guide.

## Networking Costs in AWS

Understanding the cost implications of network resources, data transfer, and cross-region communication in AWS, including strategies for optimizing networking costs.

## AWS Network Firewall

An introduction to AWS Network Firewall, a managed firewall service that provides network security and monitoring for VPC traffic, protecting against threats and unauthorized access.

