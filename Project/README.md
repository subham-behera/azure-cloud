# Azure Cloud Web Application Project

## Project Overview

This project is an Azure Internship Project focused on deploying a scalable and secure web application using various Azure Cloud services. The architecture is designed to ensure high availability, security, and scalability, following industry best practices.

## Objectives

- Deploy a web application using Azure Virtual Machines (VMs) and other Azure services.
- Ensure secure communication and access management between different components.
- Implement scalability and redundancy using Azure's Load Balancer and Virtual Machine Scale Sets.

## Architecture Overview

The project consists of the following key components:

1. **Azure Virtual Networks (VNet):**
   - **VNet-1**: Contains the frontend VMs that host the web application.
   - **VNet-2**: Hosts the Jump VM and database server. VNet peering is enabled to allow secure communication between VNet-1 and VNet-2.

2. **Jump VM:**
   - Acts as a secure gateway for administrators to connect to internal resources.

3. **Frontend VMs:**
   - Host the web application, configured with a web server to serve frontend files.

4. **Backend VM:**
   - Hosts the backend services and database. Configured with Node.js and MySQL.

5. **Load Balancer:**
   - Distributes incoming traffic across frontend VMs to ensure high availability.

6. **Azure DNS:**
   - Maps a domain name to the public IP of the Load Balancer.

## Step-by-Step Setup

### 1. Resource Group Creation
   - Created a resource group in the Azure portal to manage all related resources.

### 2. Virtual Network Setup
   - Created two Virtual Networks (VNets) and configured subnets.
   - Enabled VNet peering to allow communication between the VNets.

### 3. Virtual Machine Deployment
   - Deployed VMs for frontend, backend, and database services.
   - Configured a Jump VM for secure administration access.
   - Installed necessary software like web servers, Node.js, and MySQL.

### 4. Load Balancer Configuration
   - Set up an Azure Load Balancer to distribute traffic to the frontend VMs.
   - Configured health probes to ensure traffic is only directed to healthy instances.

### 5. Domain and DNS Configuration
   - Purchased a domain name and mapped it using Azure DNS Service.
   - Configured the domain to point to the Load Balancer's public IP.

### 6. Security Implementation
   - Applied Network Security Groups (NSGs) to control inbound and outbound traffic.
   - Used a Jump VM as the only entry point to the VNet.
   - Enabled encryption for data protection and used Azure Key Vault for managing secrets.

### 7. Monitoring and Logging
   - Integrated Azure Monitor and Application Insights for performance monitoring and alerting.

### 8. Backup and Disaster Recovery
   - Configured Azure Backup for regular backups of VMs and databases.
   - Set up Azure Site Recovery for disaster recovery planning.

## Best Practices Followed

- **Security**: Implemented NSGs, used Jump VM for secure access, and encrypted data.
- **Scalability**: Enabled auto-scaling for frontend VMs and used Load Balancer for traffic management.
- **Cost Management**: Set up cost alerts, considered reserved instances, and right-sized resources.
- **Compliance**: Used Azure Policy for governance and RBAC for access control.

## Conclusion

This project successfully deployed a secure and scalable web application on Azure, following best practices to ensure performance, security, and cost-efficiency. The architecture is designed to handle varying loads while maintaining high availability and reliability.
