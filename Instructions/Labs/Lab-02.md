# Lab 2 - Onboard Machines

## Lab scenario



### Task 1: Onboard Microsoft Defender for Endpoint Device

In this task, you will on-board a device to Microsoft Defender for Endpoint.

>**VERY IMPORTANT:** If you completed the labs for "Module 2 - Exercise 1" of this course AND have been saving your Virtual Machines until now, you can skip this task. Otherwise, you need to onboard again the **WIN1** machine to Defender for Endpoint.

>**Important:** The next steps are done in a different machine than the one you were previously working. Look for the Virtual Machine name references.

1. Login to WIN1 virtual machine as Admin with the password: **Pa55w.rd**.  

1. In the Edge browser, go to the Microsoft 365 Defender portal at (https://security.microsoft.com) and login with the **Tenant Email** credentials if you are not currently in the portal.

1. Select **Settings** from the left menu bar, then from the Settings page select **Endpoints**.

1. Select **Onboarding** in the Device management section.

1. Select **Download onboarding package**.

1. Extract the downloaded .zip file.

1. Run the Windows Command Prompt as **Administrator** and agree to any User Account Control prompts that appear.

1. Run the WindowsDefenderATPLocalOnboardingScript.cmd file that you just extracted as administrator. **Note:** By default the file should be in the c:\users\admin\downloads directory. Answer Y to questions presented by the script. 

1. From the Onboarding page in the portal, copy the detection test script and run it in an open command window. You may have to open a new **Administrator: Command Prompt** window by typing *CMD* in the windows search bar and choose to **Run as Administrator**.

1. In the Microsoft 365 Defender portal in the Endpoints area, select **Device inventory**. You should now see your device in the list.

or 

1. Go to the Microsoft Defender portal (https://security.microsoft.com), and sign in.

1. In the navigation pane, choose Settings > Endpoints, and then under Device management, choose Onboarding.

1. Select Windows 10 and 11, and then, in the Deployment method section, choose Local script.

1. Select Download onboarding package. We recommend that you save the onboarding package to a removable drive.

1. On a Windows device, extract the contents of the configuration package to a location, such as the Desktop folder. You should have a file named WindowsDefenderATPLocalOnboardingScript.cmd.

1. Open a command prompt as an administrator.

1. Type the location of the script file. For example, if you copied the file to the Desktop folder, you would type %userprofile%\Desktop\WindowsDefenderATPLocalOnboardingScript.cmd, and then press the Enter key (or select OK).

1. After the script runs, Run a detection test.

### Task 2: Run a detection test on a Windows 10 or 11 device

1. On the Windows device, create a folder: C:\test-MDATP-test.

1. Open Command Prompt as an administrator.

1. In the Command Prompt window, run the following PowerShell command:

    ``` powershell
    powershell.exe -NoExit -ExecutionPolicy Bypass -WindowStyle Hidden $ErrorActionPreference = 'silentlycontinue';(New-Object System.Net.WebClient).DownloadFile('http://127.0.0.1/1.exe', 'C:\\test-MDATP-test\\invoice.exe');Start-Process 'C:\\test-MDATP-test\\invoice.exe'
    ```

    >**Note:** After the command runs, the Command Prompt window closes automatically. If successful, the detection test is marked as completed, and a new alert appears in the Microsoft Defender portal (https://security.microsoft.com) for the newly onboarded device within about 10 minutes.

## Proceed to Exercise 3