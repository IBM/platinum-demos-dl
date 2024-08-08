---
title: Straight-through processing Technical Sales Level 3 demo
layout: preparation
banner: images/Prep-banner.png
---

<span id="top"></span>

| DEMO OVERVIEW |  |
| :--- | :--- |
| **Scenario overview** | This demo shows how the Cloud Pak for Business Automation enables straight-through processing, using a customer refund example. |
| **Demo products** | Cloud Pak for Business Automation |
| **Demo capabilities** | Workflow; Decision management; Operational intelligence |
| **Sales guidance** | Download the sales guidance document <a href="./files/Straight-through Processing Platinum Demo - Sales guidance.pdf" target="_blank" rel="noreferrer">here</a>. |
| **Demo intro slides** | Download the Introduction and Overview slides <a href="./files/Straight-through Processing Platinum Demo - Intro deck.pptx" target="_blank" rel="noreferrer">here</a>. This is a short deck of customer-facing slides that sets the context for the demo. |
| **Demo script** | This demo script has multiple tasks that each have multiple steps. In each step, you have the details about what you need to do (**Actions**), what you can say while delivering this demo step (**Narration**), and what diagrams and screenshots you will see. <br/><br/> This demo script is a suggestion, and you are welcome to customize based on your sales opportunity. Most importantly, practice this demo in advance. If the demo seems easy for you to execute, the customer will focus on the content. If it seems difficult for you to execute, the customer will focus on your delivery. |
| **Customer-ready <br/> demo video** | View the demo video <a href="https://ibm.box.com/s/3kyuqlhaqqzshbstwjiwgzclg2gmo3vy" target="_blank" rel="noreferrer">here</a>. This is a short, but detailed, hands-on walkthrough of the scenario. The video is customer-ready.<br/><br/>Potential uses of this video are:<br/><br/>1. Familiarize yourself with the details of this scenario <br/>2. Gain customer agreement that they would like to have a tech-seller do a deep-dive demo of this scenario <br/>3. Use as a prospecting tool to generate customer interest in applying these capabilities |
| **Required versions** | Cloud Pak for Business Automation as a Service (or Cloud Pak for Business Automation V23.0.1) |
| **How to get support** | • Open a support case at <a href="https://techzone.ibm.com/help" target="_blank" rel="noreferrer">IBM Technology Zone Help</a> regarding issues with reserving and provisioning Tech Zone environments.<br/>• IBMers, contact <a href="https://ibm.enterprise.slack.com/archives/C06HT5PHLN9" target="_blank" rel="noreferrer">#ba-techlcd-support</a>  regarding issues with setting up and running this demo. |

## **GET ACCESS TO AN ENVIRONMENT**

**Cloud Pak for Business Automation as a Service (SaaS)**

This demo is preinstalled on Cloud Pak for Business Automation as a Service. IBM maintains multiple SaaS tenants that can be reserved and accessed by IBMers or Business Partners. <br/>
• IBMers who already have permanent access to a demo tenant can log in <a href="https://www.automationcloud.ibm.com/" target="_blank" rel="noreferrer">here</a>. <br/>
• IBMers and Business Partners who do not already have access can reserve <a href="https://techzone.ibm.com/collection/business-automation-saas#tab-1" target="_blank" rel="noreferrer">here</a>. (After you request the reservation, you **must** activate your subscription from the **email** invitation)


## **PREPARE TO GIVE THE DEMO**

<span id="importFlow"></span>
<details markdown="1">

<summary>1 - Open the demo launchpad </summary>

The Refund Request Demo Launchpad is used to open all the user interfaces used in the demo.<br/>
Access your IBM Cloud Pak for Business Automation as a Service tenant <a href="https://www.automationcloud.ibm.com/" target="_blank" rel="noreferrer">here</a>.

1.1 Enter your email address and log in to IBM Cloud Pak for Business Automation as a Service.<br/><img src="./images/Prep1.1.png" width="800" /><br/>
1.2 Click the dropdown menu in the top left corner of the screen.<br/><img src="./images/Prep1.2.png" width="800" /><br/>
1.3 Set the **Current environment** to **Production**.<br/><img src="./images/Prep1.3.png" width="800" /><br/>
1.4 Click **Run**.<br/><img src="./images/Prep1.4.png" width="800" /><br/>
1.5 Click **Business Automation Apps**.<br/><img src="./images/Prep1.5.png" width="800" /><br/>
1.6 The **Refund request use case** demo launchpad should now appear.<br/><img src="./images/Prep1.6.png" width="800" /><br/>

**[Go to top](#top)**

</details>

<span id="importFlow"></span>
<details markdown="1">

<summary>2 - Open the process diagram for refund request without straight-through processing</summary>

You will use Process Designer to open the **Refund Request without STP** process diagram.

<inline-notification text="Currently the navigation to open Process Designer depends on the SaaS tenant you are using, which is indicated by the link that appears after clicking <strong>Hector</strong>."></inline-notification>

2.1 Click **Hector, the Process Analyst**.<br/><img src="./images/Prep2.1.png" width="800" /><br/><br/>Make note of the link that appears.<br/>
 <img src="./images/Prep2.1a.png" width="300" /><br/><br/>
2.2 Copy the **Business Automation Studio** URL and open it in a new browser tab. Click **Business Automations**.<br/><img src="./images/Prep2.2.png" width="800" /><br/><br/>
2.3 Click **Workflow**.<br/><img src="./images/Prep2.3.png" width="800" /><br/>
2.4 Click **Open** on the **Refund Request** tile (you may need to page through the **Business automations**).<br/><img src="./images/Prep2.4.png" width="800" /><br/>
2.5 Inside the process app, click **Processes**, and then click **Request Refund without STP**.<br/><img src="./images/Prep2.5.png" width="800" /><br/><br/>
2.6 The **Refund Request without STP** process diagram will open.<br/>
<inline-notification text="This will be the tab to display when you start the demo."></inline-notification><br/>
<img src="./images/Stu_3.7.png" width="800" /><br/>
<br/>

<br/>

**[Go to top](#top)**
</details>

<span id="importFlow"></span>
<details markdown="1">
<summary>3 - Open the task list and populate several in-flight tasks</summary>
<inline-notification text="Currently the interface used for the task list depends on the SaaS tenant you are using."></inline-notification>

In this step, you will open the task list view in a new tab and populate some in-flight process instances so there are tasks in the inbox.

3.1 Go to the Refund Request Demo Launchpad (pictured below) and click **Sam, the Refund Investigator**.<br/><img src="./images/Prep3.1.png" width="800" /><br/>
 • If you see a **Workplace** (1), then follow the steps below. If you see the **automatically-generated URLs** (2), skip to <a href="#altsection3">here</a>.<br/><img src="./images/3.1-workplace-or-urls.png" width="800" /><br/>
3.2  From **Workplace**, click **Start Workflow**.<br/><img src="./images/3.2-start-workflow.png" width="800" /><br/>
3.3 Click the **Request Refund** tile (1) (you may need to scroll down). Click **Launch** (2).<br/><img src="./images/Prep3.3.png" width="800" /><br/>
3.4  Repeat **two more times** to generate three tasks. You should now see at least three tasks in the inbox. Leave the task inbox open.<br/><img src="./images/3.3-three-tasks.png" width="800" />
<inline-notification text="The tasks will be automatically deleted after 12 hours to keep things clean for other users."></inline-notification><br/>
<a id="altsection3"></a>

<span id="importFlow"></span>
<details markdown="1">
<summary>3a - Open the task list and populate several in-flight tasks (Process Portal only) </summary>

In this step, you will open the task list view in a new tab and populate some in-flight process instances so there are tasks in the inbox.

3.1 Go to the Refund Request Demo Launchpad (pictured below) and click **Sam, the Refund Investigator**.<br/><img src="./images/Prep3.1.png" width="800" /><br/>
<inline-notification text="If you see <strong>automatically-generated URLs</strong>, then follow these steps. Otherwise, for <strong>Workplace</strong> use section 3 above."></inline-notification><br/>
3.2 Copy the automatically-generated URL for **Process Portal** (Navigator Work Dashboard is not supported for process creation), then paste it to a new browser tab.<br/><img src="./images/two.png" width="800" /><br/>
3.3 Under **Launch**, click **Refund Request** three times to generate a few new processes.<br/><img src="./images/three.png" width="800" /><br/>
3.4 Three new tasks should appear in the **Work** inbox.<br/><img src="./images/four.png" width="800" /><br/>
3.5 Leave this tab open for the demo. If you prefer Navigator you can close it, go back and use the automatically-generated URL to open Navigator and then navigate to the Work Dashboard.<br/>
</details>
<br/>
**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>4 - Open the process dashboard</summary>
In this step, you will you will open the **Refund Request dashboard** in a new tab.

4.1 Go to the Refund Request Demo Launchpad (pictured below), and click **Tom, the Business Analyst**.<br/><img src="./images/Prep4.1.png" width="800" /><br/>
4.2 Business Performance Center will open in a new tab. Click the **Refund Request (RR) - Week 1** dashboard.<br/><img src="./images/Stu_5.2.png" width="800" /><br/>
4.3 The **Refund Request (RR) - Week 1** dashboard will open.<br/><img src="./images/Stu_5.3.png" width="800" />

**[Go to top](#top)**
</details>

<span id="importFlow"></span>
<details markdown="1">
<summary>5 - Import ADS Decision Model</summary>

You will use a new browser tab to open Business Automation Studio.

5.1 In the Refund Request Demo Launchpad click **Emma, the Rules Manager**.<br/><img src="./images/Prep5.1.png" width="800" /><br/>
<br/>Make note of the link that appears.<br/><img src="./images/Prep2.1a.png" width="300" /><br/><br/>
5.2 Copy the **Business Automation Studio** URL and open it in a new browser tab. Click **Business Automations**.<br/><img src="./images/Prep2.2.png" width="800" /><br/><br/>
5.3 Click **Create (A)** then click **Decision automation (B)**.<br/><img src="./images/Prep5.3.png" width="800" /><br/>
5.4 Enter **STP-Refund** into the **Name** field **(A)**, then click **Create (B)**.<br/><img src="./images/Prep5.4.png" width="800" /><br/><br/>
5.5 Download the decision model file: <a href="./files/STP-Refund.zip" target="_blank" rel="noreferrer">STP-Refund.zip</a>.<br/><br/>
5.6 Click **New decision (A)**.<br/><img src="./images/Prep5.6.png" width="800" /><br/><br/>
5.7 Click **Import decision service (A)**, then click **Browse (B)**.<br/><img src="./images/Prep5.7.png" width="800" /><br/><br/>
5.8 Select the **STP-Refund.zip** file from your download location **(A)**, then click **Open (B)**.<br/><img src="./images/Prep5.8.png" width="800" /><br/><br/>
5.9 Click **Import**.<br/><img src="./images/Prep5.9.png" width="800" /><br/><br/>
5.10 Click **Refund Processing** to open the decision service.<br/><img src="./images/Prep5.10.png" width="800" /><br/><br/>
5.11 Click **Refund Processing-dmo** to open the decision model.<br/><img src="./images/Prep5.11.png" width="800" /><br/><br/>
5.12 The decision model will be displayed. <br/><img src="./images/Prep5.12.png" width="800" /><br/><br/>

**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>6 - Open the 'Focus Corp - Your Returns and Refunds' page</summary>

In this step, you will open the **Focus Corp - Your Returns and Refunds** page in a new tab. This is where you will demonstrate how to submit refund requests as a customer.

6.1 Go to the Refund Request Demo Launchpad, and click **Anna, the Customer**.<br/><img src="./images/Prep6.1.png" width="800" /><br/>
6.2 The **Focus Corp - Your Returns and Refunds** page will open. <br/><img src="./images/Stu_7.2.png" width="800" /><br/>

**[Go to top](#top)**

</details>

Click [here](demo-script) to go to the **Demo script** on the next tab.
