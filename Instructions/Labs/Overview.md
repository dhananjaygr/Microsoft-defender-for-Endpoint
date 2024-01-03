# Microsoft Defender for Endpoint 

## Overview

Microsoft Defender for Endpoint is an advanced threat protection solution designed to help organizations secure their endpoints, such as desktops, laptops, and servers. Formerly known as Microsoft Defender Advanced Threat Protection (ATP), it is a part of the Microsoft Defender suite of security products. 

### Key features of Microsoft Defender for Endpoint

1. **Endpoint Security**: Microsoft Defender for Endpoint focuses on securing endpoints, which are individual devices within an organization's network. This includes protection for Windows-based devices, macOS, Linux, and mobile devices.

2. **Threat Protection**:
The solution offers comprehensive threat protection by utilizing a combination of advanced threat intelligence, machine learning, and behavioral analysis. It helps identify and block a wide range of sophisticated threats, including malware, ransomware, and zero-day exploits.

3. **Advanced Analytics**: Microsoft Defender for Endpoint includes advanced analytics capabilities, allowing organizations to gain insights into their security posture. It provides detailed reports and analytics to help security teams understand the nature of threats and take proactive measures.

4. **Automated Investigation and Response**:
One of the key features is its ability to automate threat investigation and response. The platform can detect, investigate, and respond to security incidents automatically, reducing the workload on security teams and accelerating the response time.

5. **Threat and Vulnerability Management**:
The solution provides tools for managing and mitigating vulnerabilities within the organization. It helps prioritize and remediate security vulnerabilities on endpoints to reduce the attack surface.

6. **Integration with Microsoft 365 Security Center**:
Microsoft Defender for Endpoint integrates seamlessly with the Microsoft 365 Security Center. This integration enables security teams to have a centralized view of security incidents and manage security policies across various Microsoft 365 services.

7. **Real-time Security Alerts**: The platform delivers real-time security alerts to ensure that organizations are promptly informed about potential security threats. These alerts enable security teams to take immediate action to protect their network.

8. **Continuous Monitoring**: Microsoft Defender for Endpoint operates in real-time, providing continuous monitoring of endpoint activities. This constant vigilance helps detect and respond to threats as they emerge, ensuring a proactive approach to security.

9. **Compliance and Secure Configuration**: The solution helps organizations achieve and maintain compliance with industry standards and regulations. It also assists in enforcing secure configurations on endpoints to align with best security practices.

10. **Cloud-Powered Security**: Leveraging Microsoft's cloud infrastructure, Defender for Endpoint benefits from the scalability and intelligence of the cloud. This ensures that organizations have access to the latest threat intelligence and updates in real-time.


## Sandbox Scenario
Contoso is a global organization with a complex IT infrastructure that includes a combination of on-premises data centers and cloud-based resources. They are looking to enhance their security posture by deploying Azure Sentinel, Microsoft's cloud-native security information and event management (SIEM), and security orchestration automation and response (SOAR) solution. Additionally, Contoso aims to onboard its cloud resources and servers to Azure Sentinel to gain better visibility and proactive threat detection and response capabilities.

By implementing a robust log analytics and threat detection program, Contoso aims to proactively identify and mitigate threats, reduce the risk of security breaches, and maintain a strong security posture in an ever-evolving threat landscape. This approach will enable Contoso to stay ahead of potential threats and protect its digital assets effectively.

## About the Sandbox

Using this environment, You'll be able to explore complete features and offerings offered by Microsoft Sentinel. Please find the detailed overview of the sandbox environment below.

### Pre-provisioned resources

#### **Virtual Machines**: 

- 2 *Windows Server 2019 Datacenter* Virtual machines, virtual machine-related resources like Virtual networks, Network security groups, managed disks, Network interface cards, and IP addresses are deployed as part of the automation.

  You are recommended to use the same virtual machine throughout the lab for the best experience through out the lab.

#### **License and subscription**: 

- You'll have access to a pre-configured Microsoft user account with an active Azure subscription, a tenant, and a Microsoft 365 E5 license assigned to the user. 
   
  User account has assigned as Owner at subscription and Global administrator at the tenant level. You need to use the same user account throughout the lab to get the most out of the lab. 

#### **Azure Credits**: 

- You have been given a quota of **$83 USD** which includes the running cost of Pre-deployed resources, license cost, and other resources deployed while running through the lab.

  You will receive **cost alerts** at 50%, 75%, 90%, 95%, and 100% of the allotted Azure Credit being spent, sent to your registered email address.

  You can visit the Azure Subscription page to check the current Azure credit spend and Analysis on **Cost analysis** tab under the Cost Management option.

  ![Picture 1](../media/o1.jpg)

#### **Duration and Deletion of sandbox**:  

- The sandbox environment will be active for **30 days/730** hours from the time of registration. 
- The allowed uptime of the virtual machine is **40 hours**.
- Virtual machines will automatically **shut down** when not in use or if left idle. This feature is enabled in virtual machines to minimize the Azure spend.
- when 100% of Azure credits are spent, the sandbox environment will get automatically deleted without any prior notification. To retain the environment for a longer period and to get the most out of the environment, please follow the best practices mentioned below.

#### **Best practices**: 

- **Resources usage**: Please stop the virtual machines and other resources when not in use in order to minimize the Azure spend.

- **Azure Cost Analysis**: Maintain a practice of checking the Cost Analysis report of the assigned Azure subscription oftenly to check the Azure spend so that enviornment for a longer duration of time.

- **Alert notifications**: Make sure to check your registered email's inbox for any alert-related mails. Alerts give you can head start to keep your Azure spending in control and to plan out the remaining credits in the best way possible.
## Lab guide Content:

You will have access to a lab guide which is a reference material to assist you in getting started with the exploration. You are encouraged to explore Microsoft Defender for Endpoint further based on your interests and preferences.

- Lab 01 - Implement Microsoft Defender for Endpoint
- Lab 02 - Onboard Machines
- Lab 03 - End to end EDR (Incident, Alerts, Actions & Live Responses)
- Lab 04 - Vulnerability Management and Mitigation
- Lab 05 - Configure & Test Defender for Endpoint capabilities
- Lab 06 - Simulate & Investigate Attacks
- Lab 07 - Setup an evaluation Lab

### Azure services and related products

- Log Analytics Workspace
- Microsoft Defender for Cloud
- Microsoft Defender for Endpoint
- Microsoft Entra ID
- Microsoft Sentinel
