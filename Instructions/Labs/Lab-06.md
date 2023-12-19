# Lab 3 - Conduct a Drive-by URL attack using Attack Simulation training

## Lab scenario

## Lab objectives (Duration: 60 minutes)

## Architecture Diagram

Holly Dickson is concerned that some of the users at Adatum may require training about avoiding URL links to familiar websites that are either fake or have been hacked. This type of attack is known as a Drive-by URL attack. With this type of attack, a target receives an email containing a URL link, and when the target selects the link, they are taken to a website that runs background code whose sole purpose is to gather information about the target or deploy arbitrary code to their device. As part of her pilot project, Holly has decided to use the Microsoft 365 Attack simulation training feature to determine her users' susceptibility to Drive-by URL attacks.

### Task 1: Configure and launch a Drive-by URL attack 

In a Drive-by URL attack, the website attempting to lure the target will typically be a well-known website that has been compromised in some fashion, or a clone of a well-known website itself. The hacker hopes that familiarity with the website builds trust in the target, to the point where the target feels that it's safe to select the URL link. Holly wants to create a Drive-by URL attack using a rip-off of the Tailspin Toys website. Tailspin Toys is a nationally known toy store that is constantly offering promotions on TV and throughout social media. Holly wants to use this familiarity with the Tailspin Toys name brand to offer an enticing promotion for free toys as part of her attack simulation training. This will enable her to see how many Adatum employees are susceptible to this type of attack. 

In the prior lab, you created a simulation that was sent to all Adatum users. You also used an existing payload template for the simulation. In this lab exercise, you will only roll out the simulation to Lynne Robbins, and you will create your own custom payload.  

1. On LON-CL1, in your Edge browser, you should still be logged into Microsoft 365 as **Holly Dickson**. 

2. After the previous lab exercise, you should still be in the **Microsoft Defender** portal. If not, then in the **Microsoft 365 admin center**, under the **Admin centers** group in the left-hand navigation pane, select **Security**.

3. In the **Microsoft Defender** portal, you should still be on the **Attack simulation training** page; if not, then in the left-hand navigation pane, under the **Email & collaboration** section, select **Attack simulation training**.

4. On the **Attack Simulation training** page, the **Overview** tab is displayed by default. Select the **Simulations** tab, and then select the **+Launch a simulation** option that appears on the menu bar. This initiates the **Simulation** wizard.

5. On the **Select Technique** page in the **Simulation** wizard, scroll down and select the **Drive-by URL** option. Under this option, select the **View details of Drive-by URL** link. This opens a **Drive-by URL** pane on the right. Review the **Description** and the **Simulation steps** for this type of attack. When you're done, close the **Drive-by URL** pane and select **Next**.

6. On the **Name Simulation** page, enter **Custom payload** in the **Simulation name** field and then select **Next**.

7. On the **Select payload and login page**, the **Global payloads** tab is displayed by default. Select the **Tenant payloads** tab, and then select **+Create a payload** on the menu bar. This initiates the **Payload** wizard.

8. On the **Select type** page of the **Payload** wizard, the **Email** option should be selected by default (if not, select it now). Select **Next**. 

9. On the **Select Technique** page, the **Drive-by URL** attack type should be selected by default (all other options are disabled since you already selected this option back in step 5). Select **Next**.

10. On the **Payload Name** page, enter the following information: <br/>

	- Payload name: **Free gift offer**
	- Description: **This payload is for Drive-by URL threats offering free prizes and gifts that are too good to be true**

11. Select **Next**.

12. On the **Configure Payload** page, enter the following information: <br/>

	- From name: **Klemen Sic**
	- From email: **klemens@tailspintoys.com**
	- Email subject: **Free toy giveaway promotion from Tailspin Toys**
	- Select a URL you want to be your phishing link: select the **Select URL** button, which opens a pane of predefined phishing link URLs; select **https://www.prizegives.com** from the list of fictitious URLs (to quickly find this URL, enter **prizegives** in the Search box). and then select **Confirm** 
	- Theme: **Personalized Offer**
	- Industry: **Retail**
	- Current Event: **Yes**
	- Select the language for payload : **English** 
	- Email message: Under the Text tab in this **Email message** section, enter the following text in the message box; this message will be displayed in the body of the email message: **Tailspin Toys is offering you a FREE, one-time only giveaway of a toy of your choice as part of our 25th anniversary celebration! Please click on the following link to select the toy of your choice:** 
	- After entering the prior message, select the **Phishing link** button that appears just above the message box (to the right of **Dynamic tag**). In the **Name Phishing Url** dialog box that appears, enter **Free25thAnniversaryGift@tailspintoys.com** in the **Name** field and then select **Confirm**.

	The message should now appear as: 

	Tailspin Toys is offering you a FREE, one-time only gift of the toy of your choice as part of our 25th anniversary celebration! Please click on the following link to select the toy of your choice: **Free25thAnniversaryGift@tailspintoys.com** (make sure you have a space between the colon and the start of the link to make it look nice)

13. Select **Next**.	

14. On the **Add Indicators** page, select **Add Indicator**.

15. On the **Add Indicator** pane that appears on the right, enter the following information: <br/>

	- Select an indicator you would like to use: **Too good to be true offers**
	- Where do you want to place this indicator on payload: **From the Body of the Email**

16. A **Select Text** button will appear. Select this button.

17. In the **Select the required text** pane that appears on the right, drag your cursor from the start of the code block to the end, so that the entire code block is highlighted. This will enable the **Select** button. Select this button. This returns you to the **Add indicator** pane. 

18.  In the **Indicator Description** field, replace the default description with the following text: **Free gifts or other one-time only promotional giveaways**.

19. Select inside the **Indicator Preview** area to see a preview of the indicator message. Then select outside the **Indicator Preview** field to exit the preview. 

20. Select the **Add** button at the bottom of the **Add Indicator** pane.

21. On the **Add Indicators** page, the indicator that you just created should be displayed. Select **Next**.

22. On the **Review Payload** page, review the entered information. If anything needs to be changed, select the appropriate **Edit** option to make the change, or select **Back** to enter any of the information in the Configure section. Once everything is correct, select **Submit**. After a few moments you will receive a confirmation stating **New payload created**. Select **Done**. 

23. On the **Select payload and login page** window, the **Free gift offer** payload that you just created should appear in the list. Select the check box to the left of the **Free gift offer** payload, and then select **Next**. 

24. On the **Target Users** page, verify the **Include only specific users and groups** option is selected (if not, select it now), and then select **+Add Users**. 

25. In the **Add Users** pane that appears, in the **Search for Users or Groups** field at the top of the pane, enter **Lynne** and then hit Enter. In the list of users that appears whose name starts with Lynne, select **Lynne Robbins** and then select **Add 1 User(s)**.

26. On the **Target Users** page, Lynne Robbins should be displayed as the targeted user. Select **Next** and then select **Next** again on the **Exclude users** page. 

27. On the **Assign Training** page, under the **Preferences** section, the **Assign training for me (Recommended)** option should be selected by default (if not, select it now). Select the **Due Date** field. In the drop-down menu that appears, select **7 days after Simulation ends** and then select **Next**.

28. On the **Select Phish landing page** window, the **Global landing pages** tab should be displayed by default. Select the **Microsoft Landing Page Template 1** name to preview the page. 

29. A preview of the **Microsoft Landing Page Template 1** appears in the pane on the right. This preview panel provides an example of what the landing page will look like when someone experiences a Drive-by URL attack and the simulation uses **Microsoft Landing Page Template 1**. Scroll down through this preview panel and review the features of this template. When you're finished, select the **Close** button at the bottom of the preview panel. 

30. You will now look at some of the other landing page templates until you find one that you want to use for this simulation. On the **Select Phish landing page** window, select one of the other templates (select the name of the template and not its checkbox). Examine the preview panel and note how the landing page for this template is different from **Microsoft Landing Page Template 1**. When you're finished, select the **Close** button at the bottom of the preview panel.

31. Repeat the prior step and select another template. Note how this template is different from the other two you looked at.<br/>

	Repeat this step as many times as you would like until you find a template that you want to use for this simulation. Once you're satisfied with a template, select the checkbox for that template on the **Select Phish landing page** and then select **Next**.

32. On the **Select end user notification** page, choose how you want the end user to be notified. For the purpose of this lab, select **Microsoft default notification (recommended)**. In the list of notifications that appears, configure the following notifications:

	 - Microsoft default positive reinforcement notification - set **Delivery preferences** to **Deliver after simulation ends**
	 - Microsoft default training reminder notification - set **Delivery preferences** to  **Weekly**

33. Select **Next**.

34. On the **Launch Details** page, select the **Launch this simulation as soon as I'm done** option and then select **Next**.

35. On the **Review Simulation** page, review the entered information. If anything needs to be changed, select the appropriate **Edit** option to make the change. Once everything is correct, select **Submit**. It may take a few minutes before you receive a confirmation stating **Simulation has been scheduled for launch**. Select **Done**.  <br/>

	**Note:** Once the simulated drive-by URL attack is launched, an email should be sent to Lynne Robbins. It can take up to 15 minutes for the email to be generated. Rather than waiting for the email to be generated, you will validate the email and review the diagnostic results of the attack in Exercise 7, task 5 of this lab.

36. Leave your Edge browser and all tabs open and proceed to the next exercise.

### Task 2: Validate the simulated Drive-by URL attack

In Lab 6, Exercise 6, you configured and launched a simulated Drive-by URL attack. In this task, you will review the results of the simulated Drive-by URL attack that you launched. When you configured this attack, you selected Lynne Robbins as the target of the attack; therefore, Lynne should have received the email that you configured in the Attack simulation training. You'll verify that Lynne received this email, you'll have her respond to the email to see what happens when a user falls for a Drive-by URL attack, and you'll review the results associated with the simulated attack.

1. Switch to **LON-CL2**. On LON-CL2, in the Edge browser, you should have a tab open containing Lynne Robbins' Outlook mailbox from the earlier alert notification tasks. 

2. In Lynne's Outlook Inbox, you should see the email that was sent by the Attack Simulator that's from **Klemen Sic** (klemens@tailspintoys.com). The subject of the email is **Free toy giveaway promotion from Tailspin Toys**. Do not open the email, since like the previous alert emails, the link inserted in the email doesn't appear to work when you open the email. Instead, simply select the email to view it in the Outlook preview pane. 

3. In the email, you should recognize the message that appears, which you configured when you created this attack simulation in Exercise 6. The purpose of this message is to trick the user into thinking this is a legitimate email, when in fact, it's a Drive-by URL attack. 

4. To test this simulated attack, select the **Free25thAnniversaryGift@tailspintoys.com** link. Note what happens - the simulated drive-by URL attack displays a web page that indicates you were just phished by your IT team. It instructs you that legitimate sounding sites such as **https://www.prizegives.com**, which was the site linked to the **Free25thAnniversaryGift@tailspintoys.com** link, have been compromised by malicious attackers. So even though you may see the underlying www.prizegives.com site and you think it's legitimate, it's in fact been compromised. This site also shows you a list of information that could have been captured had this been a real attack. 

5. In your Edge browser, select the tab containing Lynne's Outlook mailbox. Note the additional email that arrived in her Inbox from the **Security and Compliance Team**. This is a legitimate email that was sent to Lynne. When you configured the simulated spear phishing attack, one of the options you selected was to send a weekly Microsoft default training reminder notification.

6. In the **Outlook** tab in your Edge browser, select the picture of Lynne Robbins in the upper-right corner of the window. In Lynne's profile window that appears, select **Sign out**.

7. Once Lynne is signed out, close the Edge browser.

8. Switch back to **LON-CL1**.

9. On LON-CL1, in your browser session where you are logged in as Holly Dickson, you should still be on the **Attack simulation training** page. Select the **Custom payload** simulation to view the diagnostic results that were captured for this simulation.

10. A **Custom payload** page should appear. Review all the information collected for this simulated attack. When you're finished, select the **X** in the upper right-hand corner of the window to close it. 

11. Leave your browser open in LON-CL1. Close all tabs EXCEPT for the **Home | Microsoft 365** and **Home | Microsoft 365 admin center** tabs.

# Proceed to Lab 6 - Exercise 7
 
