# Module 1 - Mitigate threats using Microsoft 365 Defender

**Note** Successful completion of this demo depends on completing all of the steps in the  [Pre-requisites document](00-prerequisites.md). 

## Use the Microsoft 365 Defender portal

In this task, you will familiarize yourself with the Microsoft 365 Defender portal capabilities.

- Home (Dashboard)
- Incidents & Alerts
- Hunting
- Action Center
- Threat analytics
- Secure Score
- Endpoints
- Vulnerability management
- Email & Collaboration
- Cloud apps
- Reports
- Settings
- Permissions

1. If you are not already at the Microsoft Defender Security Center in your browser, go to the Microsoft Defender Security Center at (https://security.microsoft.com) logged in as Admin for your tenant.

1. In the **Home** dashboard you can overall view of your secure status. You can customize the view by **Add cards** or removing cards. To remove a card, select the ellipsis (...) on a card.
1. Next select **Incidents & Alerts**. This will expand the menu choices below. This is where investigations are performed.
1. Do the same with **Hunting** to expose the **Advanced hunting** Query page. 
    1. You can run KQL queries here.
1. Selecting **Actions & Submissions** will expose the **Action Center** and **Submissions**
1. Select **Threat analytics**. This page provides insights into the Common Vulnerabilities and Exposures (CVE) you need to track
1. Select the **Secure Score** and explore the tabs. Take a look at **Recommendations** here.
1. Select **Endpoints** and **Device Inventory** options are available. You can onboard devices here or work with an existing inventory.
1. Also in the **Endpoints** section is **Vulnerability management**. Vulnerability management has a Dashboard where yu can look review your Exposure score.
1. Another capability within **Endpoints** is **Evaluations & simulations**. The **Evaluation lab** allows you to setup isolated devices for exploring malware.
1. In the **Email & collaboration** section are the Defender for Office 365 capabilities. **Investigations** is where you see results of Automated investigation and Response (AIR) threat investigations.
1. Also in **Email & collaboration** are **Polices & rules**. You will configure **Threat & Alert** polices here.
1. Scroll down to **Cloud apps**. This the **Microsoft Defender for Cloud Apps** service section. Under **App governance** is where you set app policies.
1. The next section is where you can find **Reports** for the Microsoft 365 Defender services, **AUdit**, where you can enable tracking of admin actions, and **Permissions** and **Settings**.
1. In **Permissions** you can configure **Azure AD** and **Endpoint** roles.
1. **Settings** is where general configuration such as timezone and email notifications are entered, plus granular settings for Endpoints, Identities and Device discovery.
1. Select **Settings**, then **Endpoints**. You can view and add **Licenses** here. Next select **Advanced features**. Scroll thorough the list of features, but don't make any changes now.
1. Lastly, leave **Settings** and on the main, left menu list select **More resources**. You should see cards or tiles with links for **Microsoft Purview Compliance**, **Azure Active Directory** and other capabilities not directly part of **Microsoft 365 Defender**. Select the **Open** button for **Microsoft Purview Compliance**. This will open the compliance portal.


or 

Objective:
To identify and mitigate vulnerabilities on endpoints using Microsoft Defender for Endpoint.

Prerequisites:
Microsoft Defender for Endpoint account with administrative privileges.
A test environment with devices running Microsoft Defender for Endpoint.
Lab Steps:
1. Access Microsoft Defender Security Center:

    - Open a web browser and navigate to https://security.microsoft.com.
    - Log in with your administrator credentials.

1. Navigate to Security Recommendations:

    - Go to the "Security recommendations" section.

1. Review Vulnerability Recommendations:

    - Identify and review the recommendations related to vulnerabilities.

1. Prioritize Vulnerabilities:

    - Prioritize vulnerabilities based on severity and potential impact.

1. Access Device Inventory:

    - Go to the "Endpoint security" or "Devices" section to view the device inventory.

1. Identify Affected Devices:

    - Use the device inventory to identify devices affected by prioritized vulnerabilities.

1. Apply Security Baselines:

    - Check and apply security baselines to enforce security configurations.

1. Deploy Updates and Patches:

    - Initiate the deployment of security updates and patches to address identified vulnerabilities.

1. Monitor Update Status:

    - Monitor the update status to ensure patches are successfully applied.

1. Perform Regular Scans:

    - Schedule and perform regular vulnerability scans.

1. Configure Automated Remediation:

    - Set up automated remediation actions for common vulnerabilities.

1. Investigate and Remediate Incidents:

    - In case of security incidents, follow incident response procedures to investigate and remediate.

1. Monitor Compliance:

    - Ensure devices remain compliant with security configurations and policies.

1. Documentation and Reporting:

    - Document the actions taken to mitigate vulnerabilities.
    - Generate reports to track the status of vulnerabilities and mitigation efforts.

1. Continuous Improvement:

    - Regularly review and update vulnerability management processes based on emerging threats.

Conclusion:
Congratulations! You have successfully completed the lab to manage and mitigate vulnerabilities using Microsoft Defender for Endpoint. Regularly repeat these steps to maintain a secure endpoint environment.

Note: This lab guide provides a high-level overview. Refer to Microsoft Defender for Endpoint documentation for detailed instructions and the latest information.

## You have completed the lab.