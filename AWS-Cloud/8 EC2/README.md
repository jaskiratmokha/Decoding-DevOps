# Amazon EC2 (Elastic Compute Cloud)

Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides resizable compute capacity in the cloud. It allows users to quickly scale up or down to handle changes in requirements or spikes in traffic, paying only for the capacity they actually use. EC2 offers a wide selection of instance types optimized to fit different use cases, from general-purpose computing to memory-intensive workloads and high-performance computing.

## Overview

Amazon EC2 is a virtual machine service in AWS, providing virtualized computing resources with various configuration options, storage types, and networking features. It's a foundational service in AWS and integrates seamlessly with other AWS services.

## Virtual Machines (EC2)

EC2 instances are virtual servers that run on Amazon's cloud infrastructure. They can be configured with various options:

- **Operating System (OS):** Choose from a variety of operating systems including Windows, Linux, and macOS.
- **CPU:** Select the desired number of virtual CPUs (vCPUs) for your instance.
- **RAM:** Choose the amount of memory (RAM) required for your workload.
- **Network Attached Storage:**
  - **Elastic Block Store (EBS):** Persistent block storage volumes.
  - **Elastic File System (EFS):** Scalable file storage for use with EC2 instances.
- **Hardware Attached:**
  - **Instance Store:** Temporary block storage physically attached to the host computer.
- **Network Card:** Configure network settings such as speed and IP address.
- **Firewall:** Control inbound and outbound traffic using Security Groups.
- **Bootstrap Script (User Data):** Run scripts with root privileges on instance launch for setup and configuration tasks.

## Use Cases

EC2 instances are versatile and can be used for various purposes, including:

- Installing updates and software.
- Downloading files from the internet.
- Running applications and services.

## Instance Types

EC2 offers different instance families optimized for specific workloads:

- **General Purpose:** Balanced computing, memory, and network resources.
- **Compute Optimized:** High CPU performance for compute-intensive tasks.
- **Memory Optimized:** High memory capacity for memory-intensive workloads.
- **Storage Optimized:** High disk I/O performance for storage-intensive applications.

## Purchasing Options

Users can choose from several purchasing options based on their requirements and budget:

- **On-Demand:** Pay for compute capacity by the second with no long-term commitments.
- **Reserved:** Reserve instances for 1 or 3 years for discounted pricing.
- **Convertible:** Reserved instances with the flexibility to change instance type, OS, and region.
- **Spot Instances:** Bid for unused capacity at lower prices, suitable for short-lived or flexible workloads.
- **Dedicated Hosts:** Rent dedicated physical servers for compliance or licensing requirements.

## Additional Features

- **Elastic IP:** Static IP addresses for EC2 instances, allowing for failover and masking instance failures.
- **Placement Groups:** Strategies for grouping EC2 instances based on availability, proximity, or hardware.
- **ENI (Elastic Network Interfaces):** Virtual network cards for EC2 instances with various configuration options.
- **EC2 Hibernate:** Standby mode for instances, preserving RAM state for faster startup.
- **Instance Recovery:** Restore EC2 instances with the same configurations and settings after failure.

## Limits and Considerations

- **Instance Limits:** AWS imposes default limits on the number of EC2 instances per account, based on vCPU usage.
- **Resource Management:** Proper resource management is essential to optimize costs and performance.
- **Security:** Follow best practices for securing EC2 instances and data.


