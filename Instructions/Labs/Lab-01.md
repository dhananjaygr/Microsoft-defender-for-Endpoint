# Lab 01 - Implement Microsoft Defender for Endpoint

## Lab overview

In this lab, participants will immerse themselves in the practical implementation of Microsoft Defender for Endpoint. The primary goal is to equip participants with the skills and knowledge necessary to fortify the security infrastructure of organizational endpoints.

## Lab scenario

The objective of this lab is to provide hands-on experience in setting up and configuring Microsoft Defender for Endpoint, a comprehensive endpoint security solution. Participants will learn how to enhance the security posture of their organization's endpoints by implementing various features and policies offered by Defender for Endpoint.

- **Hands-On Experience:** Participants will actively engage with the Microsoft Defender for Endpoint platform, gaining practical experience in the setup and configuration processes. This hands-on approach allows them to familiarize themselves with the actual steps involved in deploying and managing Defender for Endpoint.

- **Understanding Endpoint Security:** The lab emphasizes the significance of endpoint security, highlighting Defender for Endpoint as a robust solution. Participants will delve into the functionalities and capabilities of the platform, understanding how it plays a pivotal role in safeguarding organizational endpoints.

- **Comprehensive Security Solution:** Defender for Endpoint is positioned as a comprehensive security solution. Throughout the lab, participants will explore the diverse features and components that contribute to its comprehensive nature. This includes aspects such as threat detection, response mechanisms, and integration with other security tools.

## Lab objectives

In this lab, you will perform the following:

- Task 1: Setup Defender for Endpoint  
- Task 2: Configure Roles
- Task 3: Configure Device Groups
- Task 4: Create Baseline Policies

## Estimated timing: 60 minutes

## Architecture Diagram

  ![Picture 1](../Media/arch-1.1.png)

### Task 1: Setup Defender for Endpoint  

In this task, you will perform the initialization of the Microsoft Defender for the Endpoint portal.

1. Inside the Lab-VM, double click on the  **Microsoft Edge** shortcut.

    ![Picture 1](../Media/edgeshortcut.png)

1. In the Edge browser, go to the [Microsoft Defender portal](https://security.microsoft.com).

1. In the **Sign in** dialog box, copy and paste Email/Username: <inject key="AzureAdUserEmail"></inject> and then select Next.

1. In the **Enter password** dialog box, copy and paste Password: <inject key="AzureAdUserPassword"></inject> and then select **Sign in**.

1. On the **Microsoft Defender** portal, from the left-navigation menu, select **Settings (1)** from the left.

1. On the **Settings** page select **Device discovery (2)**. 

    ![Picture 1](../Media/devicediscovery.png)

    >**Note:** If you do not see the **Device Discovery** option under **Settings**, log out by selecting the top-right circle with your account initials and choose **Sign Out**. Other options to consider are refreshing the page, waiting for 20-25 minutes, or opening the page in private mode (InPrivate). Afterwards, log in again using the **Tenant Email** credentials.

1. In the Discovery setup make sure **Standard discovery (recommended)** is selected. 
    
    >**Hint:** If you do not see the option, refresh the page.

    ![Picture 1](../Media/standarddiscovery.png)

    
### Task 2: Configure Roles

In this task, you will configure roles for use with device groups.

1. Open a new tab, and browse to the [Azure portal](https://portal.azure.com).

1. In the **Sign in** dialog box, copy and paste **Email/Username (1)**: <inject key="AzureAdUserEmail"></inject> and then select **Next (2)**.

    ![Picture 1](../Media/portal1.png)

1. In the **Enter password** dialog box, copy and paste **Password (1)**: <inject key="AzureAdUserPassword"></inject> and then select **Sign in (2)**.

    ![Picture 1](../Media/portal2.png)

1. On the **Stay signed in?** dialog box, select the Don’t show this again check box and then select **No**.

    ![Picture 1](../Media/portal3.png)

1. If a **Welcome to Microsoft Azure** popup window appears, click **Maybe Later** to skip the tour.

1. In the Azure portal, in the **Search resources, services, and docs** text box at the top of the Azure portal page, type **Microsoft Entra ID (1)**, and then select **Microsoft Entra ID (2)**.

    ![Picture 1](../Media/microsoftentra.png)

1. Select **Groups (1)** and then click on **New group (2)**.

    ![Picture 1](../Media/groups.png)

    ![Picture 1](../Media/newgroup.png)
    
1. Enter the below details for the New group page:

   |Setting|Value|
    |---|---|
    |Group Type| **Microsoft 365 (1)** |
    |Group Name| **Sg-IT (2)** |
    |Microsoft Entra roles can be assigned to the group| **Yes (3)** |

1. Under **Owners** section, click on **No owners selected** and select the **ODL_User <inject key="DeploymentID" enableCopy="false"></inject>** from the list and then click on **select**.

1. Under **Members** section, click on **No members selected** and select the **ODL_User <inject key="DeploymentID" enableCopy="false"></inject>** from the list and then click on **select**.

   **Note**: Make sure you have selected **Group type** as Microsoft 365.

1. Select **Create (6)** and click on **Yes (7)**. 

    ![Picture 1](../Media/newgroup(1).png)

    ![Picture 1](../Media/yes.png)

1. On the **Groups | All groups** page, if you are not able to see the group that you created, **Refresh (1)** the page.

    ![Picture 1](../Media/refresh.png)

1. Navigate back to the **Microsoft Defender** portal tab. In the Microsoft Defender portal select **Settings (1)** from the left menu bar, then select **Endpoints (2)**. 

    ![Picture 1](../Media/Microsoftdefenderportal.png)

1. Select **Roles (1)** under the permissions.

1. Select the **Turn on roles (2)** button.

    ![Picture 1](../Media/turnonroles.png)

1. Select **+ Add Role**.

    ![Picture 1](../Media/addroles.png)

1. In the Add role dialog enter the following, and select **Next (4)**:

    |General setting|Value|
    |---|---|
    |Role name|**Tier 1 Support (1)**|
    |Permissions|**Live Response capabilities (2)** > **Advanced (3)**|

    ![Picture 1](../Media/tier1.png)

1. On the **Add role** page, select **sg-IT (1)** and then select **Add selected groups (2)**. Make sure it appears under **Azure AD user groups with this role (3)**.

    ![Picture 1](../Media/adduser.png)

1. Select **Submit (4)** and Done. If you receive an error while saving the role, refresh the page and try again.

    ![Picture 1](../Media/sgit.png)

   > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
   > - Navigate to the Lab Validation Page, from the upper right corner in the lab guide section.
   > - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
   > - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
   > - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help you out.

### Task 3: Configure Device Groups

In this task, you will configure device groups that allow for access control and automation configuration.

1. In the Microsoft Defender portal select **Settings (1)** from the left menu bar, then select **Endpoints**. 

1. Select **Device groups (2)** under the permissions area.

1. Select **+ Add device group (3)** icon.

    ![Picture 1](../Media/devicegroup.png)    

1. Enter the following information on the General tab:

    |General setting|Value|
    |---|---|
    |Device group name|**Regular (1)**|
    |Remediation level| **Full-Remediate threats automatically (2)**|

1. Select **Next (3)**.

    ![Picture 1](../Media/group.png)

1. On the **Devices** tab, for the OS condition select **Windows Server 2022 (1)** and select **Next (2)**.

    ![Picture 1](../Media/windowsserver2022.png)

1. On the **Preview devices** tab, select **Next**.

1. On the User access tab, select **sg-IT** and then select **Add selected groups** button. Make sure it appears under **Azure AD user groups with access to this device group**.

1. Select **Submit**

1. Select **Done**.

1. Device group configuration has changed. Select **Apply changes** to check matches and recalculate groupings.

    ![Picture 1](../Media/applychanges.png)

1. You are going to have two device groups now; the **Regular** you just created and the **Ungrouped devices (default)** with the same remediation level.

    ![Picture 1](../Media/devicegroups1.png) 

### Task 4: Create Baseline Policies

In this task, your objective is to implement the Windows Intune security baseline, which offers a comprehensive set of recommended settings essential for securely configuring devices running Windows. This includes configuring browser settings, PowerShell configurations, and specific settings for security features such as Microsoft Defender Antivirus.

1. Open another tab and browse to the [Microsoft Intune admin center](https://intune.microsoft.com/?ref=AdminCenter#home).

1. From the left navigation pane, select **Endpoint security (1)**, under **Overview** section, select **Security Baselines (2)**.

1. On the **Endpoint security | Security baselines**, select **Security Baseline for Windows 10 and later (3)**.

    ![Picture 1](../Media/securitybaseline.png)

1. On the **MDM Security Baseline | Profiles** page, select **+ Create profile**.

    ![Picture 1](../Media/createprofile(1).png)

1. On the **Create profile** page, under the **Basics** tab, enter any **name (1)** of your choice and **description (optional)**, then select **Next (2)**.

    ![Picture 1](../Media/mdm-policy.png)

1. On the **Configuration settings** tab, review all configurations by expanding each one. If you want to edit any of the configurations, feel free to make your changes. Select **Next**.

1. Keep the **Scope tags** tab as default, select **Next**.

1. On the **Assignments** tab, under **Included groups**, select **Add groups**, on the **Select groups to include** page, choose **Sg-IT**, and click on **Select**. Select **Next**.

1. On the **Review + create** page, select **Create**.

1. After the policy is created, you will be able to view it in the **MDM Security Baseline | Profiles** section.

    ![Picture 1](../Media/securitybaseline1.png)

## Review
In this lab, you have completed the following:

- Setup Defender for Endpoint 
- Configured Roles
- Configured Device Groups
- Created Baseline Policies

## You have successfully completed the lab. Click on Next >>.
