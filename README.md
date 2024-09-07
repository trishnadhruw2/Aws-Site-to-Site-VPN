
Setting Up a Site-to-Site VPN between AWS VPCs in Mumbai Region and Singapore Region

Here’s a quick overview:

Objective: Enable secure communication between EC2 instances in different regions.
Steps: Created VPCs and subnets, launched EC2 instances, set up VPN connections, and updated routing tables.
Outcome: Seamless connectivity was achieved, and instances in Mumbai and Singapore can now communicate securely.

Key Takeaways:

Understanding cross-region VPC connectivity.
Configuring VPN connections for secure communication.
Troubleshooting common connectivity issues.


Introduction:
In this project, I demonstrate how to set up a site-to-site VPN between two AWS VPCs located in different regions (Mumbai and Singapore). The goal is to establish secure communication between EC2 instances deployed in subnets across these VPCs.

Prerequisites:
AWS account with necessary permissions
Basic understanding of AWS VPCs, subnets, and EC2 instances
Familiarity with VPN concepts
Step-by-Step Guide:
Create VPCs:

Mumbai Region: VPC1 with CIDR block 10.1.0.0/16
Singapore Region: VPC2 with CIDR block 10.2.0.0/16
Create Subnets:

Mumbai Region: Subnet1 with CIDR block 10.1.0.0/24
Singapore Region: Subnet2 with CIDR block 10.2.0.0/24
Launch EC2 Instances:

Mumbai Region: EC2 Instance1 in Subnet1
Singapore Region: EC2 Instance2 in Subnet1
Set Up VPN Connections:

Create a Virtual Private Gateway (VGW) in mumbai region.
Attach VGW to the respective VPC.
Create a Customer Gateway (CGW) in the Mumbai VPC.
Set up a VPN connection between the VGW and CGW in Mumbai.
Configure Routing:

Update route tables in both VPCs to direct traffic to the VPN connection.
Testing Connectivity:

Test connectivity by pinging EC2 Instance2 from EC2 Instance1.
Configuration Files:
Include relevant configuration snippets, such as VPC settings, subnet details, and routing tables.
Results:
The setup was successful, and EC2 instances in different regions can communicate via the VPN.
Troubleshooting:
Common issues and solutions, such as ensuring security groups and network ACLs allow traffic.
Conclusion:
By following these steps, you can securely connect VPCs in different AWS regions, enabling seamless communication between resources.
