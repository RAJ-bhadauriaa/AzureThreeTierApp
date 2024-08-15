# Insights and Learnings

## Project Overview

This project involved creating a three-tier architecture on Azure, incorporating a Web Tier, App Tier, and Database Tier. Each tier was isolated within its own subnet, and network security groups (NSGs) were used to control the flow of traffic between them.

### Key Learnings

- **Network Security Groups (NSGs):** 
  We learned how to effectively use NSGs to secure each tier of the architecture. Proper configuration of inbound and outbound rules is crucial to ensuring that traffic only flows between the correct tiers.

- **Load Balancers:**
  Configuring both public and internal load balancers allowed us to balance the traffic between VMs while maintaining security. The public load balancer managed incoming web traffic, while internal load balancers facilitated communication between the app and database tiers.

- **Virtual Networks and Subnets:**
  Dividing the architecture into different subnets ensured a high level of isolation between the tiers. This design improves security by preventing direct communication between the web and database tiers.

### Challenges

- **Quota Limits:**  
  One challenge encountered was reaching Azure resource quota limits, particularly when deploying multiple VMs. We learned to monitor quota usage and how to request quota increases from the Azure portal.

- **IIS Server Configuration:**
  Hosting a frontend site on a Windows VM required setting up the IIS server. While straightforward, it was important to ensure all files were placed in the correct directories and that IIS services were properly configured.

### Future Improvements

- **Scalability:**
- This setup is scalable and can be extended by adding more VMs to the backend pools of each load balancer.
  The current architecture is designed to be scalable. In the future, we could explore adding autoscaling for VMs, integrating Azure SQL Database, or using Azure Application Gateway for enhanced routing.

- **Monitoring and Alerts:**  
  Setting up Azure Monitor for real-time alerts on system performance and traffic patterns could provide additional oversight and automatic alerts.

---

This project has provided valuable hands-on experience with Azure's core services and reinforced the importance of designing secure, scalable architectures for cloud applications.
