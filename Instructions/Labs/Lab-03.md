# Lab 03 - End to end EDR (Incident, Alerts, Actions & Live Responses)

## Lab overview

This lab encompasses the end-to-end process of incident detection, alert generation, response actions, and live responses within an EDR framework. Participants will gain hands-on experience in managing security incidents from detection to resolution, utilizing the live response feature for real-time remediation.

## Lab scenario

Creating Incidents in Microsoft 365 Defender involves identifying potential security threats from various alerts and promptly responding to mitigate risks. Security analysts investigate these alerts to confirm their severity and impact.

- **Incident Detection**: Participants will learn how EDR systems detect security incidents by monitoring endpoint activities and behaviors.
Understanding the criteria for identifying potential incidents is a key focus.

- **Alert Generation**: The lab emphasizes the automatic generation of alerts based on detected incidents. Participants will explore how EDR platforms categorize and prioritize alerts for efficient incident response.

- **Response Actions**: Practical response actions to mitigate the impact of incidents will be explored.
Participants will learn to leverage EDR capabilities to respond to incidents effectively.

- **Live Responses**: The lab introduces participants to the concept of live responses for real-time remediation.
Practical scenarios will be simulated where participants actively respond to ongoing security incidents.

## Lab objectives

In this lab, you will perform the following:

- Task 1: Create Incident and alerts
- Task 2: Actions & Live Responses

## Architecture Diagram

![Picture 1](../Media/Architecture-03.3.PNG)

### Task 1: Create Incident and alerts

In this task, you will run two simulated attacks to explore the capabilities of Microsoft Defender for Endpoint.

1. Open a new tab, and browse to the [Microsoft 365](https://www.office.com). 

    >**Note:** If it shows you the **Sign in** dialog box, copy and paste * Email/Username: <inject key="AzureAdUserEmail"></inject> and then select Next. In the **Enter password** dialog box, copy and paste * Password: <inject key="AzureAdUserPassword"></inject> and then select **Sign in**.

    >**Note:** On the **Welcome to Microsoft 365** select **>**. Select **>** on **As an administrator, you have additional tools to manage your company**, and select **✔** on **Next, we'll show you some tips to help you personalize and organize Microsoft 365 your way**. Close all the pop-ups.

1. You will be redirected to the home page of Microsoft 365. Select **Install and more (1)**, and choose **Install Microsoft 365 apps (2)** to download all the Microsoft 365 apps to the desktop.

    ![Picture 1](../Media/installmore.png)

1. On the **My account** page, under **Office apps & devices** select **Install office**.

1. After downloading, select **Open file** to initiate the installation process. Once the installation is complete, close the installation pop-up.

1. If the Microsoft 365 Defender portal is not open in your Microsoft Edge browser, open a new tab and go to (https://security.microsoft.com).

1. In the **Sign in** dialog box, copy and paste * Email/Username: <inject key="AzureAdUserEmail"></inject> and then select Next.

1. In the **Enter password** dialog box, copy and paste * Password: <inject key="AzureAdUserPassword"></inject> and then select **Sign in**.

1. From the menu, under **Endpoints**, select **Evaluation & tutorials (1)** and then select **Tutorials & simulations (2)** from the left side.

   ![Picture 1](../Media/incident1.png)

1. Select the **Tutorials (1)** tab.

1. Under *Automated investigation (backdoor)* you will see a message describing the scenario. Below this paragraph, click **Read the walkthrough (2)**. A new browser tab opens which includes instructions to perform the simulation.

   ![Picture 1](../Media/readthewalkthrough.png)

1. In the new browser tab, locate the section named **Run the simulation** (page 5, starting at step 2) and follow the steps to run the attack. 

    > **Hint:** The simulation file *RS4_WinATP-Intro-Invoice.docm* can be found back in Microsoft defender portal, just below the **Read the walkthrough** you selected in the previous step by selecting the **Get simulation file** button. 

1. After downloading the file, select **Open file**. It will open with **Microsoft Word** and enter the password as `WDATP!diy#`.

1. Select **Continue** to activate the word.

1. On the **Activate office** pop-up, copy and paste the Username and password provided in the environment details page, and select next. 

1. On the **Stay signed in to all your apps**, select **No, sign in to this app only**.

    ![Picture 1](../Media/staysigned.png)

1. Select **Accept** on the **Accept the license agreement** page, and close the privacy matters page.

1. Click **Enable Editing** if the document opens inProtectedView. If you see a subsequent security warning about macros being disabled. Close the Word file. 

1. To unblock the document, navigate to its location in File Explorer. In File Explorer, right-click the document, and select Properties. In the General tab, check the **Unblock (1)** option under Security, and select **OK (2)**.   

    ![Picture 1](../Media/unblock.png)

1. Re-open the word file from the File Explorer and enter the password as `WDATP!diy#` after re-opening click on **Enable Content** and click on **OK**. 

1. In the Command prompt pop-up press any key to close. 
      
    >**Note:** **Congrats – you’re done running the attack!** The attack simulation ends here. A real attacker, if successful, would likely continue to scan for information, send collected reconnaissance information to a command-and-control (C&C) server, and use this information to move laterally and pursue other attractive targets. Next, let’s review and investigate the Defender for Endpoint alerts that surfaced in the simulated attack.

    >**Note:** Incidents & Alerts should start to appear 15-30 minutes after the simulated backdoor is launched.

1. Open the Microsoft 365 Defender portal select **Incidents & alerts** from the left menu bar, then select **Incidents**.

    ![Picture 1](../Media/incident3.png)

1. Select the new incident named "**Multi-stage incident involving Initial access & Persistence on one endpoint**" to load its details.

    ![Picture 1](../Media/incident4.png)

    >**Note:** If you are unable to see the incident, please wait for 15-30 minutes; it will appear.

1. From the left menu bar, choose **Incidents & Alerts (1)**, then click on **Alerts (2)** to view all generated alerts. You can select any of the alerts to check the details.

    ![Picture 1](../Media/alerts.png)

### Task 2: Actions & Live Responses

1. In the Microsoft 365 Defender portal select **Incidents & alerts** from the left menu bar, then select **Incidents**.

    ![Picture 1](../Media/incident3.png)

1. Select **Multi-stage incident involving Initial access & Persistence on one endpoint**, on the **Multi-stage incident involving Initial access & Persistence on one endpoint (1)** page, select any one of the active alerts, on the alerts page under **Details (2)** section, view each and every details present inside the details section.

    ![Picture 1](../Media/active-alerts.png)

    ![Picture 1](../Media/details.png)

1. After viewing, choose **Manage alerts**. On the **Manage alert** page, follow these instructions: select **Save**, and then close the alert page.
    
    |**Settings**|**Value**|
    |------------|---------|
    |Status|**Resolved**|
    |Assign to|**Assign to me**|
    |Classification|**Select as per your choice**|
    |Comment (Optional)|**Add a comment** as per your choice|

1. Now, you will be on the incident page for **Multi-stage incident involving Initial access & Persistence on one endpoint**. Select the **Evidence and Responses (1)** tab; here, you can see all the listed evidence. Choose each piece of evidence to check the corresponding responses.

    ![Picture 1](../Media/evidence.png)

1. If you select any of the pieces of evidence, on the evidence page, choose **See in device timeline** to view the detailed report of the evidence.

    ![Picture 1](../Media/seedevice.png)

## Review
In this lab, you have completed the following:

- Created Incident and alerts
- Explored Actions & Live Responses

## You have successfully completed the lab.
