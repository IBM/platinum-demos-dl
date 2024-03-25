---
title: Process and task mining <br/>Technical Sales Level 3 demo
layout: preparation
banner: images/Process_mining_prep_banner.jpg
---

<span id="top"></span>

| DEMO OVERVIEW | |
| :---         | :--- |
| **Scenario overview** | This demo shows how IBM’s process mining capabilities are used to discover and analyze business processes and identify areas for improvement. A customer account closing example is used to showcase how process mining helps an organization meet regulatory requirements while also reducing process execution cost. |
| **Demo products** | Cloud Pak for Business Automation |
| **Demo capabilities** | Process mining; Task mining |
| **Sales guidance** | Download the sales guidance document <a href="./files/Process and Task Mining Platinum Demo - Sales guidance.pdf" target="_blank" rel="noreferrer">here</a>. |
| **Demo intro slides** | Download the Introduction and Overview slides <a href="./files/Process and Task Mining Platinum Demo - Intro deck.pptx" target="_blank" rel="noreferrer">here</a>. This is a short deck of customer-facing slides that sets the context for the demo. |
| **Demo script** | A complete demo script is on the second tab above. You can download a printer-ready PDF of the demo script <a href="./files/Process and Task Mining Platinum Demo - PDF script.pdf" target="_blank" rel="noreferrer">here</a>. <br/><br/>This demo script has multiple tasks, that each have multiple steps. In each step, you have the details about what you need to do (**Actions**), what you can say while delivering this demo step (**Narration**), and what diagrams and screenshots you will see. <br/><br/> This demo script is a suggestion, and you are welcome to customize based on your sales opportunity. Most importantly, practice this demo in advance. If the demo seems easy for you to execute, the customer will focus on the content. If it seems difficult for you to execute, the customer will focus on your delivery. |
| **Sales enablement video** | View the enablement video <a href="https://ibm.box.com/s/zbk59qe79twwzbb7m5gv9yemamew30kj" target="_blank" rel="noreferrer">here</a>. This video is for enablement purposes only (IBMers and Business Partners) and is not customer-ready. |
| **How to get support** | • Open a support case at <a href="https://techzone.ibm.com/help" target="_blank" rel="noreferrer">IBM Technology Zone Help</a> regarding issues with reserving and provisioning Tech Zone environments.<br/>• IBMers, contact <a href="https://ibm.enterprise.slack.com/archives/C06HT5PHLN9" target="_blank" rel="noreferrer">#ba-techlcd-support</a>  regarding issues with setting up and running this demo. |

## **INSTALL THE DEMO**
<span id="spamID"></span>
<details markdown="1">

<summary>1 - Provision a Technology Zone demo environment</summary><br/>
1. Reserve a Technology Zone demo environment <a href="https://techzone.ibm.com/collection/process-mining-with-task-mining-demo-and-etl/environments" target="_blank" rel="noreferrer">here</a>.<br/><br/>
2. On the reservation form, be sure to select **Enable** for **VPN Access**. <br/><br/><inline-notification text="If you do not enable VPN access, you will <strong>not</strong> be able to access the Process mining workspace directly from a web browser on your local computer. "></inline-notification> <br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/prep-1.png" width="600" /><br/>
3. Wait until your reservation status is ready, and then access your Technology Zone environment using the link in the reservation email. You may also use the IBM Technology Zone’s **My Library** → **My Reservations** page. (You can either keep refreshing the **My Reservation** page or wait for a confirmation email.)<br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/prep-10.png" width="400" /><br/>

**[Go to top](#top)**

</details>

## **PREPARE TO GIVE THE DEMO**
<span id="spamID"></span>
<details markdown="1">

<summary>1 - Open the IBM Process Mining workspace</summary><br/>
Use the TechZone published services to open the IBM Process Mining workspace in a browser on your local computer:

1. Find the publish services at the top of your TechZone reservation page: <br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/Prep-1-1.png" width="800" /><br/>
2. In your local web browser, enter the Process Mining Web Client URL appended with **/signin#!** <br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/Prep-1-2.png" width="800" /><br/>
3. Sign in using **'maintenance.admin'** for the **Username** and **'IBMDem0s!'** for the **Password**. <br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/prep-11.png" width="300" /><br/>
4. From the **Process mining** workspace, click the **Account Closure** tile. <br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/Prep3.4a.png" width="800" /><br/><inline-notification text="If the <strong>Account Closure</strong> tile is not in the <strong>Recent processes</strong> list, scroll down (1) to the <strong>All processes</strong> list and click <strong>Account Closure</strong> (2)."></inline-notification> <br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/Prep3.4b.png" width="800" /><br/>
5. Click the **Manage** tab (1) and then **Data source** (2) from the left navigation panel. The **Data source** tab is now open, and you're ready to give the demo. <br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/prep-9.png" width="800" />
<br/>

**[Go to top](#top)**

</details>

<span id="altremote"></span>
<details markdown="1">

<summary>2 - Alternate remote desktop configuration</summary><br/>
1. Use **MS Remote Desktop App** (available on the Mac App Store and Microsoft Windows Apps store) to create a Remote Desktop instance using the RDP Published Service.
2. Locate the **RDP Published Services** in your reservation.
<br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/prep-published-services.png" width="800" />
3. Enter the **Published Service URL** for **PC name**.
<br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/prep-published-service-URL.png" width="800" />
4. Enter **'Administrator'** for the **Username** and **'IBMDem0s!'** for the **Password**. Click **Log in**.
<br/>

**[Go to top](#top)**

</details>

***

Click [here](demo-script) to go to the **Demo script** on the next tab.


