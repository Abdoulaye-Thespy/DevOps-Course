# Becoming a Cloud Prationner Part 2
## Module 1: Security
Note:
- AWS Shield, AWS WAF for sql injection attacks
- Topic A: Shared responsibility Model
    1. AWS is responsible of security of the cloud
        - Global infrastructure security: AWS ensures the security of its data centers, network, and hardware infrastructure.
        - Hypervisor security: AWS protects the virtualization layer that separates customer instances.
        - Managed services security: AWS manages the security of its managed services, such as AWS Lambda, Amazon RDS, and Amazon S3.   

    2.  We are responsible of security in the cloud
        - Security group configurations: Customers define and manage the inbound and outbound network traffic rules for their instances.
        - Operating system and network firewall configurations: Customers are responsible for securing their operating systems, including patching, firewall configurations, and anti-malware protection.
        - Application security: Customers must secure their applications, including code vulnerabilities, data encryption, and access controls.
        - Data protection: Customers are responsible for protecting their data at rest and in transit, including encryption and backups.
        - Identity and access management: Customers manage user access, authentication, and authorization to their AWS resources.
- Topic B: AWS IAM (Policies and roles)
    - IAM policies are JSON documents that define the permissions granted to IAM users, groups, and roles.
    - IAM roles are similar to users but are meant to be assumed by other AWS entities, such as EC2 instances or Lambda functions.

- Topic C: AWS organizations
- Topic D: Application security
## Module 2: Storage
- Topic A: Block storage with EBS
- Topic B: File storage with EFS
## Module 3: Compute in the Cloud
- Topic A: Amazon EC2 (Demos create and pricing)
- Topic B: Amazon EC2 Autoscaling
- Topic C: Elastic load balancing