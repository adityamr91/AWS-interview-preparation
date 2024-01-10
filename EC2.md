Q: What is Amazon EC2?<br />
Answer: Amazon EC2 (Elastic Compute Cloud) is a cloud computing service provided by Amazon Web Services (AWS) that offers virtual servers, known as instances, for running applications in the cloud. It provides scalability, flexibility, and cost-effectiveness by allowing users to easily scale up or down their compute capacity based on their needs.<br />

Q: What is Security Group in Amazon EC2?<br />
Answer: Amazon Security group acts like a virtual firewall for you EC2 instances, they control both inbound and outbound traffic. It acts as a protective barrier, allowing you to define rules that determine which traffic is allowed to access your instances. Security groups operate at the instance level, meaning you can assign one or more security groups to each instance.<br />

Q: What is Amazon Machine Image (AMI)?<br />
Answer: An Amazon Machine Image (AMI) is a special type of pre-configured virtual machine image that is used to create virtual servers (EC2 instances) in the AWS environment. You must specify an AMI during the launch of EC2 instance. This is a faster way to setup an EC2 instance with pre-configured software, no manual setup required. Multiple EC2 instances can be launched from a single AMI.<br />

Q: What is instance types?<br />
Answer: An instance type in Amazon EC2 refers to the specification of virtual hardware resources assigned to an EC2 instance. It defines the computing capacity, memory, storage, and networking capabilities of the instance. Each instance type has its own pricing structure and performance characteristics, allowing users to choose the most suitable option based on their specific application requirements and budget.
For example –<br />

General Purpose: Instances optimized for a balance of compute, memory, and networking resources. Example: t3.medium.<br />
Compute Optimized: Instances designed for applications that require high computational power. Example: c5.large.<br />
Memory Optimized: Instances with large memory capacity, suitable for memory-intensive workloads. Example: r5.large.<br />
Storage Optimized: Instances with high-performance storage for data-intensive workloads. Example: i3.large.<br />
GPU Instances: Instances equipped with powerful GPUs for accelerated graphics and parallel processing. Example: g4dn.xlarge.<br />

Q: Explain Stop and Start VS Terminate an Amazon Ec2 Instance?<br />
Answer: Stop and Start: When you stop an EC2 instance, the instance is temporarily halted, and the underlying resources (such as the allocated CPU and memory) are released.
The instance retains its metadata, attached storage volumes, and IP address when stopped. When you start the instance again, it is assigned a new internal IP address, but the attached storage volumes remain intact. This option is useful when you want to pause an instance temporarily without losing any data or configurations.<br />

Terminate: Terminating an EC2 instance permanently shuts it down and releases all associated resources, including the instance metadata, attached storage volumes, and IP address. This action cannot be reversed, and all data stored on the instance is lost unless it is backed up or saved in another storage solution. Termination is suitable when you no longer need the instance and want to release the associated resources to avoid ongoing costs.<br />

Q: What is the use of Regions and Availability Zones in Amazon EC2 configuration?<br />
Answer: When configuring your EC2 instances, you choose the region where you want them to be deployed geographically, and then you can select the specific availability zone within that region. This allows you to distribute your instances across multiple zones for improved fault tolerance and high availability.<br />

By leveraging regions and availability zones, you can design and deploy applications that are resilient, fault-tolerant, and provide low-latency services to users in different geographic locations.<br />

Q: How do you get charged in AWS?<br />
Answer: In Amazon EC2, you are charged based on several factors that includes –<br />

Instance Types: The primary cost in EC2 is based on the type and size of the instances you choose.<br />
Instance Hours: You are billed for the number of hours that your instances are running. In case of instance stopped state Amazon EBS volume or an Amazon EFS file system still associated with EC2, that are billed for storage.<br />
On-Demand Instances: On-Demand instances are billed per hour based on the instance type and the region in which they are running.
Reserved Instances: Reserved Instances offer discounted pricing compared to On-Demand instances. By committing to a specific term (one or three years) and payment option (all upfront, partial upfront, or no upfront), you can achieve cost savings for long-term usage.<br />
Spot Instances: Spot Instances allow you to bid on unused EC2 capacity and potentially receive instances at significantly lower prices. Spot Instance pricing fluctuates based on supply and demand, and your instances may be interrupted if the Spot price exceeds your bid.<br />
Storage: You are billed for the storage capacity you allocate for your instances, such as Amazon Elastic Block Store (EBS) volumes or Amazon Elastic File System (EFS) file systems. The cost depends on the storage type, capacity, and region.<br />
Data Transfer: Data transfer costs apply when data is transferred between different regions, availability zones, or over the internet. Data transfer within the same AWS region or availability zone is usually free.<br />
Load Balancers, Auto Scaling, and Other Services: Additional services like Elastic Load Balancer, Auto Scaling, Amazon CloudWatch, and others may have their own pricing based on their usage and configuration.<br />

Q: Explain what happens when you Reboot an EC2 Instance?<br />
Answer: Rebooting is very similar to rebooting a PC, it allows for a controlled restart of EC2 instance while preserving the instance’s identity, network configuration, and data stored on persistent storage.<br />

Rebooting an EC2 instance is a useful action for resolving certain system issues, applying updates, or refreshing the instance’s runtime environment.<br />

Q: What is Placement Group in EC2?<br />
Answer: In Amazon EC2, a placement group is a logical grouping of instances within a single Availability Zone. Using a Placement Group provides advantages such as reduced network latency and increased network throughput. It is a free feature currently available in Amazon EC2.<br />

When an instance is stopped and restarted, it continues to operate within the same Placement Group. However, it is important to note that Instances from different Availability Zones cannot be added to the same Placement Group.<br />
