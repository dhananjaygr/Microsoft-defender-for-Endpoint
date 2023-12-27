# Lab 02 - Onboard Machines

## Lab scenario

The objective of this lab is to provide participants with hands-on experience in onboarding machines to Microsoft Defender for Endpoint. It involves the process of integrating and configuring them to seamlessly connect with a security or management system. This typically includes installing necessary software, configuring settings, and ensuring compliance with security policies. In the context of Microsoft Defender for Endpoint, onboarding Windows client devices involves downloading and installing the Defender for Endpoint client, confirming successful onboarding, and configuring security policies to enhance threat protection on the Windows devices.

## Lab objectives

In this lab, you will perform the following:

- Task 1: Onboard Windows Client devices 
- Task 2: Run a detection test

## Architecture Diagram

  ![Picture 1](../Media/Architecture-02.PNG)

### Task 1: Onboard Windows Client devices

In this task, you will onboard windows client devices to Microsoft Defender for Endpoint using an onboarding script.

1. If you are not already at the Microsoft Defender portal in your browser, start the Microsoft Edge browser go to (https://security.microsoft.com) and log in with the **Tenant Email** credentials.

1. Select **Settings** from the left menu bar, then from the Settings page select **Endpoints**.

1. Select **Onboarding** in the Device Management section.

    >**Note:** You can also perform device onboarding from the **Assets** section of the left menu bar. Expand Assets and select Devices. On the Device Inventory page, with Computers & Mobile selected, scroll down to **Onboard devices.** This takes you to the **Settings > Endpoints** page.

1. In the "1. Onboard a device" area make sure "Local Script (for up to 10 devices)" is displayed in the Deployment method drop-down and select the **Download onboarding package** button. 

1. Under the *Downloads* pop-up, highlight the "WindowsDefenderATPOnboardingPackage.zip" file with your mouse and select the folder icon **Show in folder**. **Hint:** In case you don't see it, the file should be in the c:\users\admin\downloads directory.

1. Right-click the downloaded zip file and select **Extract All...**, make sure that **Show extracted files when complete** is checked and select **Extract**.

1. Right-click on the extracted file "WindowsDefenderATPLocalOnboardingScript.cmd" and select **Properties**. Select the **Unblock** checkbox in the bottom right of the Properties windows and select **OK**.

    ![Picture 1](../Media/sc200-mod2-unblock.png)

1. Right-click on the extracted file **WindowsDefenderATPLocalOnboardingScript.cmd** again and choose **Run as Administrator**.  **Hint:** If you encounter the Windows SmartScreen window, select on **More info**, and choose **Run anyway**. 
    
1. When the "User Account Control" window is shown, select **Yes** to allow the script to run and answer **Y** to the question presented by the script and press **Enter**. When complete you should see a message in the command screen that says *Successfully onboarded machine to Microsoft Defender for Endpoint*.

1. Press any key to continue. This will close the Command Prompt window.

    ![Picture 1](../Media/SC-200-img25.png)

1. Back in the Onboarding page from the Microsoft Defender portal, under the section "2. Run a detection test", copy the detection test script by selecting the **Copy** button.  

1. In the windows search bar of the virtual machine, type **CMD** and choose **Run as Administrator** on the right pane for the Command Prompt app. 

1. When the "User Account Control" window is shown, select **Yes** to allow the app to run. 

1. Paste the script by right-clicking in the **Administrator: Command Prompt** windows and press **Enter** to run it. **Note:** The window closes automatically after running the script.

1. In the Microsoft Defender portal, in the left-hand menu, under the **Assets** area, select **Devices**. If the device is not shown, complete the next task and come back to check it back later. It can take up to 60 minutes for the first device to be displayed in the portal.

     ![Picture 1](../Media/SC-200-img22.png)

    >**Note:** If you have completed the onboarding process and don't see devices in the Devices list after an hour, it might indicate an onboarding or connectivity problem.

### Task 2: Run a detection test

In this task, run the following PowerShell script on a newly onboarded device to verify that it's properly reporting to the Defender for Endpoint service.

1. Inside the Lab-VM, select **Type here to search**, and search for **CMD**, right-click on **Command Prompt** and select **Run as administrator**.

1. At the prompt, copy and run the following command:

    ```powershell
    powershell.exe -NoExit -ExecutionPolicy Bypass -WindowStyle Hidden $ErrorActionPreference = 'silentlycontinue';(New-Object System.Net.WebClient).DownloadFile('http://127.0.0.1/1.exe', 'C:\\test-MDATP-test\\invoice.exe');Start-Process 'C:\\test-MDATP-test\\invoice.exe'
    ```
    
    >**Note**: The Command Prompt window closes automatically. If successful, a new alert appears in the portal for the onboarded device in about 10 minutes.

## Review
In this lab, you have completed the following:

- Onboarded Windows Client devices 
- Ran a detection test

## You have successfully completed the lab.
