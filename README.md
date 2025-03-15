Web Hosting Architecture: EC2-Based Deployment with Shared EFS Storage
Implementation Steps:
VPC & Network Configuration

Create a Virtual Private Cloud (VPC) and configure subnets across multiple Availability Zones (AZs) to enhance fault tolerance.
Security Groups Configuration

Define two Security Groups (SGs):
EC2 Security Group: Permits inbound traffic for SSH (22), HTTP (80), and HTTPS (443).
EFS Security Group: Allows NFS (2049) access exclusively from the EC2 Security Group to enforce secure file sharing.
EC2 Deployment

Launch two EC2 instances in distinct subnets within the VPC to ensure high availability.
Configure instances to use public IPs for external accessibility.
EFS Integration

Provision an AWS Elastic File System (EFS) and attach it to both EC2 instances.
Mount the EFS directory on each instance to enable a centralized, scalable storage solution.
Website Deployment

Store website files within the EFS-mounted directory, ensuring synchronous access across both instances.
Testing & Validation

Verify public accessibility of the hosted website via EC2 instance public IPs or an Elastic Load Balancer (ELB).
Confirm real-time file synchronization between instances by modifying web content.
Expected Outcome:
A highly available, scalable, and fault-tolerant web hosting environment leveraging EC2 instances with shared EFS storage, ensuring redundancy, data consistency, and seamless accessibility across multiple availability zones. 🚀
