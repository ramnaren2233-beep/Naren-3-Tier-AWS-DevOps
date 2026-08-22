## Task 1: Design and Configure the AWS Networking Infrastructure

A custom VPC was created for the application.

1.VPC

# Resource	          Details

VPC Name	            Naren-3Tier-VPC

VPC ID	              vpc-02ee6cb19b7fe6387

IPv4 CIDR	            10.0.0.0/16

State	                Available

2. ## Subnets

Six subnets were created and distributed across two Availability Zones.

    Subnet	            Type	          Subnet ID	                    CIDR	                      Availability Zone

Naren Web Subnet 1	  Public -A     subnet-07bbbd0d216953858	     10.0.1.0/24               aps1-az1 (ap-south-1a)

Naren Web Subnet 2	  Public -B	    subnet-044b47da2d36ccf88 	     10.0.2.0/24               aps1-az1 (ap-south-1a)

Naren App Subnet 1	  Private-A     subnet-0bb4dc4133e76a9c1         10.0.3.0/24               aps1-az1 (ap-south-1a)

Naren App Subnet 2	  Private-B     subnet-08e7db9cea295b3a4         10.0.4.0/24               aps1-az3 (ap-south-1b)

Naren DB Subnet  1	  Private-A      subnet-0dad776d0eb5fb9c6        10.0.5.0/24               aps1-az1 (ap-south-1a)

Naren DB Subnet  2	  Private -B	 subnet-03ebc86567f72a083        1.0.0.6.0/24               aps1-az3 (ap-south-1b)

Each subnet was configured to support the required number of IP addresses.


3. # Internet Gateway

An Internet Gateway was created and attached to the VPC.

  Resource	                             Details

Internet Gateway Name	              Naren-3Tier-IGW

Internet Gateway ID	                 igw-0aa4cc29a3e54fefc

VPC ID	                            vpc-02ee6cb19b7fe6387 | Naren-3Tier-VPC

State	                                Attached


4. # Elastic IP

An Elastic IP was allocated for the NAT Gateway.

Resource	                            Details

Elastic IP	                      NAT-Gateway-Elastic-IP

Allocation ID	                    eipassoc-04f456af3dd0d81b3

Purpose	                          Used for NAT Gateway

5. # NAT Gateway

A NAT Gateway was created in a public subnet.

Resource	                            Details

NAT Gateway Name	                 Naren-3Tier-NAT

NAT Gateway ID	                   nat-0b39dd633b804ac49

Subnet ID	                         subnet-07bbbd0d216953858 / Naren-Web-Public-A

Elastic IP	                       15.252.109.150

State	                             Available

The NAT Gateway provides outbound Internet access to resources in the private application subnets.

6. # Route Tables

Three route tables were created for the different network tiers.

# Public Route Table

Resource	                            Details

Route Table Name	                Naren-Public-RT

Route Table ID	                   rtb-0bb22353b11e149d4

Associated Subnets	        subnet-07bbbd0d216953858 / Naren-Web-Public-A,  subnet-044b47da2d36ccf88 / Naren-Web-Public-B

Routes:

Destination	                            Target

10.0.0.0/16                              Local

0.0.0.0/0	                           Internet Gateway

# Private Application Route Table

Resource	                             Details

Route Table Name	                Naren-App-Private-RT

Route Table ID	                  rtb-0ef2d3f5298cc3eb5

Associated Subnets	        subnet-0bb4dc4133e76a9c1 / Naren-App-Private-A,  subnet-08e7db9cea295b3a4 / Naren-App-Private-B


Routes:

Destination	                            Target

10.0.0.0/16                              Local

0.0.0.0/0	                           nat-0b39dd633b804ac49

# Private Database Route Table


Resource	                             Details

Route Table Name	                Naren-DB-Private-RT

Route Table ID	                  rtb-0cd7e20df74b7bc7e

Associated Subnets	        subnet-0dad776d0eb5fb9c6 / Naren-DB-Private-A,  subnet-03ebc86567f72a083 / Naren-DB-Private-B


Routes:

Destination	                            Target

10.0.0.0/16                              Local

The database subnets do not have a direct route to the Internet Gateway.

7. # Subnet Associations

The subnets were associated with the appropriate route tables.

Route Table	                            Associated Subnets

Public Route Table	                 subnet-07bbbd0d216953858 / Naren-Web-Public-A    subnet-044b47da2d36ccf88 / Naren-Web-Public-B 

Private Application Route Table	     subnet-0bb4dc4133e76a9c1 / Naren-App-Private-A   subnet-08e7db9cea295b3a4 / Naren-App-Private-B

Private Database Route Table	       subnet-0dad776d0eb5fb9c6 / Naren-DB-Private-A    subnet-03ebc86567f72a083 / Naren-DB-Private-B

8. # AWS Resources Summary
   
AWS Resource	                              Quantity

VPC                                            1

Public Subnets	                               2

Private Application Subnets	                   2

Private Database Subnets	                     2

Internet Gateway	                             1

NAT Gateway	                                   1

Elastic IP	                                   1

Route Tables	                                 3

















