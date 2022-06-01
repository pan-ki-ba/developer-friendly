### AWS Questions

#### **VPC CIDR Blocks**
  - CIDR blocks size can be between /16 to /28
  - First four and last IP address are not available for use
#### **Amazon VPC**
  - Logically isolated virtual network in the AWS cloud
  - **Components**
    - **Subnet**
      - Segment of a VPC's ip address range where you can place group of isolated resource/s
    - **Router**
    - **Internet Gateway**
    - **NAT Instance**
      - Enables internet access for EC2 instances in private subnets ( managed by you )
    - **NAT Gateway**
      - Enables internet access for EC2 instances in private subnets ( managed by AWS )
    - **Security Group**
      - Instance level firewall
    - **Network ACL**
      - Subnet level firewall
  - When you create a VPC, you must specify a range of IPv4 addresses for the VPC in the form of a Classless Inter Domain Routing (CIDR) block. For e.g. 10.0.0.0/16
  - VPC spans all availability zones of the region
