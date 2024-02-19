---
title: Extending business automation with RPA 300-level live demo
layout: preparation
banner: images/RPA_300_Prep_Banner.jpg
---

<span id="top"></span>

| DEMO OVERVIEW | |
| :---         | :--- |
| **Scenario overview** | This demo shows how the IBM Cloud Pak for Business Automation can be used to extend business automation with Robotic Process Automation (RPA). To illustrate this, an insurance policy quoting process is automated. |
| **Demo products** | Cloud Pak for Business Automation |
| **Demo capabilities** | RPA bots; RPA chatbots; Workflow |
| **Sales guidance** | Download the sales guidance document <a href="./files/Extending BA with RPA Platinum Demo - Sales guidance.pdf" target="_blank" rel="noreferrer">here</a>. |
| **Demo intro slides** | Download the Introduction and Overview slides <a href="./files/Extending BA with RPA Platinum Demo - Intro deck.pptx" target="_blank" rel="noreferrer">here</a>. This is a short deck of customer-facing slides that sets the context for the demo. |
| **Demo script** | A complete demo script is on the second tab above. You can download a printer-ready PDF of the demo script <a href="./files/300-BA-extending-with-rpa-Demo-Script.pdf" target="_blank" rel="noreferrer">here</a>. <br/><br/>This demo script has multiple tasks, that each have multiple steps. In each step, you have the details about what you need to do (**Actions**), what you can say while delivering this demo step (**Narration**), and what diagrams and screenshots you will see. <br/><br/> This demo script is a suggestion, and you are welcome to customize based on your sales opportunity. Most importantly, practice this demo in advance. If the demo seems easy for you to execute, the customer will focus on the content. If it seems difficult for you to execute, the customer will focus on your delivery. |
| **Customer-ready <br/> demo video** | View the demo video <a href="https://ibm.box.com/s/wnrq16fc5qs2ddpidvg03lpu6271x8du" target="_blank" rel="noreferrer">here</a>. This is a short, but detailed, hands-on walkthrough of the scenario. The video is customer-ready. <br/> <br/> Potential uses of this video are: <br/> <br/> 1. Familiarize yourself with the details of this scenario <br/> 2. Gain customer agreement that they would like to have a tech-seller do a deep-dive demo of this scenario <br/> 3. Use as a prospecting tool to generate customer interest in these capabilities |
| **Customer-facing <br/> expert guidance** | <a href="./files/RPA vs. workflow - Automation Expert Series.pdf" target="_blank" rel="noreferrer">RPA vs. workflow: It's not either/or... it's both</a> |
| **Demo architecture** | <br/> <img src="./images/Demo-Architecture.png" width="500" /> |
| **Required versions** | Cloud Pak for Business Automation V21.0.2 |
| **How to get support** | • Open a support case at <a href="https://techzone.ibm.com/help" target="_blank" rel="noreferrer">IBM Technology Zone Help</a> regarding issues with reserving and provisioning Tech Zone environments.<br/>• IBMers, contact <a href="https://ibm.enterprise.slack.com/archives/C06HT5PHLN9" target="_blank" rel="noreferrer">#ba-techlcd-support</a>  regarding issues with setting up and running this demo. |

## **INSTALL THE DEMO**

<details markdown="1">

<summary>1 - Establish access to an RPA SaaS tenant</summary><br/>

In addition to the Technology Zone provided environment, you will need access to the  <a href="https://app.wdgautomation.com/" target="_blank" rel="noreferrer">IBM RPA SaaS environment</a>. If you are already onboarded to a RPA SaaS tenant, you will need the login information. <br/><br/>

**If you are not already onboarded to a RPA SaaS tenant:**

For **IBMers**, refer to the RPA contact person to establish your RPA account in the cloud tenant.
<br/>

•	Contact your IBM RPA TechSales Geo Lead (refer to the table below) for access to your IBM local IBM RPA tenant.<br/>
•	Once onboarded, you will receive an email with account details and link to complete the onboarding. You will need this information in section 3 - Install RPA Studio, step 5.

| Region | Contact Person | Email |
| :--- | :--- | :--- |
| Business Partners | Burt Hughes | See instructions below. |
| Americas | Ryan Sparks | rmsparks@us.ibm.com |
| EMEA | Jukka Juselius | jukka.juselius@fi.ibm.com |
| AP | Jenny Khuc Mai Thuong | khuc@sg.ibm.com |


For **Business Partners**, request your own RPA Server SaaS tenant for your organization. To submit a request for an IBM server SaaS tenant, provide the following: <br/><br/>
• Company Name and CEID (which can be found in your PartnerWorld profile) <br/>
• Full Name (first and last) of the individual who will be set up as administrator of the account <br/>
• Company email address of the individual listed above (non-company email addresses will be rejected) <br/>
• Data Center choice (choose one: Dallas, Frankfurt, London, Singapore, Sao Paulo) <br/>
• Use the following subject line: **RPA BP Tenant Access Request** <br/>
• Send an email to Burt Hughes (buhughes@us.ibm.com)

<br/>

**[Go to top](#top)**

</details>
<span id="spamID"></span>
<details markdown="1">

<summary>2 - Provision a Technology Zone demo environment</summary><br/>

1. Reserve a Technology Zone demo environment <a href="https://techzone.ibm.com/collection/platinum-demos-extending-business-automation-with-RPA/environments" target="_blank" rel="noreferrer">here</a>.<br/>
2. Wait until your reservation status is **Ready** on the IBM Technology Zone’s **My Library → My Reservations** page. (You can either keep refreshing the My Reservation page or wait for a confirmation email.)<br/><img src="./images/prep-res-status-ready.png" width="300" /><br/>When your reservation is **Ready**, click the reservation tile to view the reservation details.<br/>
3. On the reservation details page, scroll down and click to open the RPA **VM Remote Console**. It is the link on the right. <br/>  <br/> <inline-notification text="Use the RPA VM Remote Console to setup and run the entire demo."></inline-notification> <br/><img src="./images/prep-rpa-remote-console.png" width="500" />
4. The console will open. Click **Full screen**.<br/><img src="./images/prep-click-full-screen.png" width="500" /> <br/>
5. Click inside the window to bring up the log in screen. Type the password '**il0vedem0s**' (those are zeros in the password). <br/><img src="./images/prep-administator-login.png" width="500" /> <br/> <inline-notification text="The first time you access the VM, you will be presented with the network option below. It is imperative to select <strong>YES</strong>. (Otherwise, the VM will not be properly configured for this demo.)"></inline-notification> <br/><img src="./images/prep-networks-yes.png" width="300" /> <br/>
6. (**Optional**) Right-click on the Windows desktop and select <strong>Display settings</strong>. Adjust the display resolution to best fit your desktop.<br/><img src="./images/prep-display-settings.png" width="300" />

<br/>

**[Go to top](#top)**

</details>
<span id="spamID"></span>
<details markdown="1">

<summary>3 - Install RPA Studio</summary><br/>

1. Open the RPA **VM Remote Console** (if it is not already open). Use the links on the reservation page. Open the link on the right. Then click to open the console in **Full screen**.<br/><img src="./images/prep-console-full-screen.png" width="500" /><br/>
2. Using File Explorer, navigate to **This PC** (1). Right click to bring up the menu, and select **Properties** (2). Click **Rename this PC** (3).<br/><img src="./images/5-This-PC-properties.png" width="500" /><br/> <inline-notification text="Log in if needed using the <strong>RPA VM Remote Desktop (RDP)</strong> password on your reservation details page."></inline-notification>
3. Enter a new computer name, which needs to be unique to your SaaS RPA tenant. Use **'WIN–your initials–your postal code'** (1). Click **Next** (2).<br/> <img src="./images/rename-your-pc.png" width="500" /> <br/>
4. Restart the VM.<br/><br/>

**Next, download, install, and log in to RPA Studio.**<br/><br/>
5. Open Chrome within the VM. Use the link provided in your RPA tenant email from section 1 to log in to the RPA cloud tenant and download the RPA Studio installer. Have your server and license information available to enter in these steps.<br/><br/>
6. Using Chrome, go to your RPA tenant server login page. <br/> <img src="./images/5.Login-RPA.png" width="800" /><br/>
7. From the server home page, click the **“i”** (top right) and then **Download Installer**. <br/> <img src="./images/6.Download-Setup.exe.png" width="800" /><br/>
8. Using File Explorer, navigate to **Setup.exe**. Then, right click and select **Run as Administrator**. <br/> <img src="./images/7.Run-setup.png" width="800" /><br/>
9. Click **Next**. <br/> <img src="./images/8.Setup-wizard1.png" width="500" /><br/>
10. Click **Next**. <br/> <img src="./images/9.Setup-wizard2.png" width="500" /><br/>
11. Accept the terms, and click **Next**. <br/> <img src="./images/10.Setup-wizard3.png" width="500" /><br/>
12. Select **Complete Install**. <br/> <img src="./images/11.Setup-wizard4.png" width="500" /><br/>
13. Click **Next** to begin the install. <br/> <img src="./images/12.Setup-wizard5.png" width="500" /><br/>
14. Click **Next** (No proxy configuration is needed so leave the box unchecked). <br/> <img src="./images/13.Setup-wizard6.png" width="500" /><br/>
15. Enter the license information, which should have been provided to you by your RPA SaaS administrator. <br/> <img src="./images/prep-image3.18.png" width="500" /><br/>
16. Wait for the install to complete. <br/> <img src="./images/15.Setup-wizard8.png" width="500" /><br/>
17. Exit the installer. If necessary, the VM will restart. <br/> <img src="./images/16.Setup-wizard9.png" width="500" /><br/>
18. Note that the desktop icons for RPA Studio will be created. <br/> <img src="./images/17.Desktop-icons.png" width="100" /><br/>
19. Open RPA Studio.<br/><img src="./images/18.RPA-Service1.png" width="500" /><br/> <inline-notification text="The <strong>IBM Robotic Process Automation Agent</strong> Windows service is set to 'delayed start,' and you must wait for it to be started. You can see it in the system tray or in the Windows services list. "></inline-notification> <br/><img src="./images/19.RPA-Service2.png" width="800" /><br/>
20. Log in to IBM RPA. To log in, first fill in your **User Name** and click **Login**. Then the interface will let you input your password. <br/><img src="./images/21.Login-to-RPA.png" width="800" /><br/>

**[Go to top](#top)**

</details>
<span id="spamID"></span>
<details markdown="1">

<summary>4 - Verify the 'Get Quote' bot is published on the RPA SaaS tenant</summary><br/>

1. Log in to your RPA SaaS tenant. <br/> <img src="./images/login-rpa-saas.png" width="800" /> <br/>
2. Click **Scripts** in the side menu. <br/> <img src="./images/prep-image4.2.png" width="800" /> <br/>
3. Initiate a search by clicking the **Search** icon. <br/> <img src="./images/search-scripts1.png" width="800" /> <br/>
4. Enter **GetQuoteFCQS** in the search field and ensure the **GetQuoteFCQS** bot script appears. <br/> <img src="./images/prep-image4.4.png" width="800" /><inline-notification text="If <strong>'GetQuoteFCQS'</strong> does not appear, continue with these steps:"></inline-notification>
5. Click the desktop icon to open IBM RPA Studio and log in. <br/><br/>
6. Click the **Open** button on the menu ribbon.<inline-notification text="Click the word <strong>Open</strong>, not the down arrow. We are opening the scripts locally, not from the repository. "></inline-notification><br/><img src="./images/31.Open-WAL1.png" width="800" /><br/>
6. Select the **Get Quote.wal** file (located in c:\WDG\WAL), and click **Open**. <br/> <br/><img src="./images/32.Open-WAL2.png" width="800" /> <br/>
7. Click the **Publish** button on the menu ribbon. <br/> <img src="./images/publish-bot1.png" width="800" /> <br/>
8. Enter the following fields: <br/>
•	Name: **GetQuoteFCQS** (1)<br/>
•	Description: **RPA demo** (2)<br/>
•	Set as production: toggle to **true** (3)<br/>

  Then click **Publish** (4). <br/><img src="./images/rpa-prep-publish-bot2.png" width="800" /><br/>

**[Go to top](#top)**

</details>
<span id="spamID"></span>
<details markdown="1">

<summary>5 - Verify the IngridKB is published on the RPA SaaS tenant</summary><br/>
<inline-notification text="First check if <strong>IngridKB</strong> is already published."></inline-notification>

1. Log in to your RPA SaaS tenant. <br/> <img src="./images/login-rpa-saas.png" width="800" /> <br/>
2. Click **Machine Learning** in the side menu. <br/> <img src="./images/verify-ingrid-machine-learning.png" width="800" /> <br/>
3. Initiate a search by clicking on the **Search** icon.<br/> <img src="./images/verify-ingrid-search-icon.png" width="800" /> <br/>
4. Enter **'IngridKB'** in the search field (1) and ensure **IngridKB** appears in the results (2). <br/> <img src="./images/verify-ingrid-search-results.png" width="800" /><inline-notification text="If <strong>IngridKB</strong> does not appear, continue with these steps."></inline-notification>
5. Download the IngridKB export file <a href="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-extending-ba-with-rpa/IngridKB.xlsx" target="_blank" rel="noreferrer">here</a>.<br/>
6. Click the desktop icon to open **IBM RPA Studio** and log in.<br/>
7. In the menu bar on the header, select the **Tools** tab.<br/> <img src="./images/prep-3-9-tools-tab.png" width="800" /><br/>
8. Click the **Machine Learning Model Builder** button.<br/> <img src="./images/prep-3-10-button.png" width="800" /><br/>
9. Complete the **Machine Learning Model Builder** form with the following information:<br/>
• In the **Name** field, type **IngridKB** (1).<br/>
• In the **Culture** field, select **English** (2).<br/>
• In the **Algorithm** field, select **Knowledge Base V2** (3).<br/>
• In the **Options** field, select **Use synonyms** (4).<br/>
• In the **File** field, select the IngridKB export file in XLSX format (5).<br/>
• Enable the **Set as production** option (6). <br/><br/>
Click **Save** (7).
<br/> <img src="./images/prep-complete-machine-learning-form.png" width="800" />

<br/>

**[Go to top](#top)**

</details>

## **PREPARE TO GIVE THE DEMO**

<span id="place2"></span>
<span id="spamID"></span>
<details markdown="1">

<summary>1 - Start the BAW server</summary><br/>

1. Open the BAW **VM Remote Console**. Use the links on the reservation page. Open the link on the left. Then click to open the console in **Full screen**. <br/><img src="./images/baw-vm-remote-console.png" width="500" /><br/>
2. Click the red **Ctrl+Alt+Del** button. <br/><img src="./images/button.png" width="300" /><br/>
3. Log in to the Administrator account using the password **IBMPlatinumDem0s!** (that is a "zero" in 'Dem0s'). <br/><br/>
4. The command window will appear automatically. (You will need to wait 5-10 minutes after the commands execute for the BAW server to be fully started.) <br/><img src="./images/command-window.png" width="500" /><br/>
5. You can now close the BAW console. The subsequent steps will be performed using the RPA VM console. <br/>

<br/>

**[Go to top](#top)**

</details>
<span id="spamID"></span>
<details markdown="1">

<summary>2 - Open the bot scripts in IBM RPA Studio</summary><br/>

1. Open the RPA **VM Remote Console** (if it is not already open). Use the links on the reservation page. Open the link on the right. Then click to open the console in **Full screen**.<br/><img src="./images/prep-console-full-screen.png" width="500" /><br/>
2. Click the desktop icon to open IBM RPA Bot Studio.<br/><br/>
3. Use the **Open** button on the menu ribbon to open the scripts.<br/><inline-notification text="Click on the word <strong>Open</strong>, not the down arrow. We are opening the scripts locally, not from the repository."></inline-notification><br/><img src="./images/31.Open-WAL1.png" width="800" /><br/>
4. Click the **Open** button (1) in the menu ribbon. Navigate to and select the **Get Quote.wal** file (2). <br/> <img src="./images/bot-script-get-quote.png" width="800" /> <br/>
5. Click the **GetQuote** routine (this action doesn't change anything functionally, but will look best during the demo). <br/> <img src="./images/33.Open-WAL3.png" width="800" /> <br/>
6. Click the **Open** button (1) in the menu ribbon, and select the **Insurance Ingrid.wal** file (2). <br/> <img src="./images/bot-script-insurance-ingrid.png" width="800" />

<br/>

**[Go to top](#top)**

</details>
<span id="spamID"></span>
<details markdown="1">

<summary>3 - Open the New Customer Quote process diagram</summary><br/>

1. First, use Firefox to open **Workflow Center**. In the Firefox bookmarks bar, open **BAW** -> **Workflow Center - Solutions**. <br/><inline-notification text="Using separate browsers for Workflow vs. Portal prevents the logins from colliding with each other. "></inline-notification> <br/><img src="./images/Process-diagram1.png" width="800" /> <br/>
2. Log in to Workflow Center using **admin/admin**. <br/> <img src="./images/Process-diagram2.png" width="800" /> <br/>
3. Under **Start Building**, **Process Apps**, click **View all**. <br/> <img src="./images/Process-diagram3.png" width="800" /> <br/>
4. Open the **New Insurance Quote** process app. <br/> <img src="./images/Process-diagram4.png" width="800" /> <br/>
5. Open the **New Insurance Quote** process definition. <br/> <img src="./images/Process-diagram5.png" width="800" /> <br/>
6. The **New Customer Quote** process definition is now open. <br/> <img src="./images/Process-diagram6.png" width="800" />

<br/>

**[Go to top](#top)**

</details>
<span id="spamID"></span>
<details markdown="1">

<summary>4 - Open the Workflow Process Portal</summary><br/>

1. Use Chrome to open **Process Portal**. In the Chrome bookmarks bar, open **BAW** -> **Process Portal**. <br/><inline-notification text="Using separate browsers for Workflow Center vs. Portal prevents the logins from colliding with each other."></inline-notification><br/><img src="./images/Process-portal1.png" width="800" /> <br/>
2. Leave the page open to the Process Portal login screen. The **username** is **customerService** and the **password** is **password**. You are now ready to show the demo. <br/> <img src="./images/Process-portal2.png" width="800" /><br/>

**[Go to top](#top)**

</details>

***

Click [here](/300-business-automation-extending-ba-with-rpa/demo-script) to go to the **Demo script** on the next tab.