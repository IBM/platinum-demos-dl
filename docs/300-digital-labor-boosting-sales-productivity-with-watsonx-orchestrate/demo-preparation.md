---
title: Boosting sales productivity with watsonx Orchestrate <br/> 300-level live demo
layout: preparation
banner: images/wxo_300_prep_banner.png
---

<span id="place1"></span>

<span id="top"></span>

<inline-notification text="<strong><strong>Attention: Safari and Chrome browser users.</strong> Please use Firefox to do this demo."></inline-notification>

| **DEMO OVERVIEW** | | 
| :---         | :--- |
| **Scenario overview** | This demo shows how watsonx Orchestrate can be used by sales representatives to assist with the upsell / cross-sell process. To illustrate this, an insurance seller uses watsonx Orchestrate to retrieve a list of customers from Salesforce and automatically send a customized offer. Developers, called ‘builders’ in watsonx Orchestrate, create the customized skills used by the agents. |
| **Demo products** | watsonx Orchestrate |
| **Demo capabilities** | Salesforce skill; watsonx.ai generative AI skill; Microsoft Outlook skill; Embedded decision engine skill|
| **Demo script** | A complete demo script is on the second tab above. <br/><br/> This demo script has multiple tasks that each have multiple steps. In each step, you have the details about what you need to do (**Actions**), what you can say while delivering this demo step (**Narration**), and what screenshots you will see.<br/><br/>This demo script is a suggestion, and you are welcome to customize based in your sales opportunity. Most importantly, practice this demo in advance. If the demo seems easy for you to execute, the customer will focus on the content. If it seems difficult for you to execute, the customer will focus on your delivery. |
| **How to get support** | • Open a support case at <a href="https://techzone.ibm.com/help" target="_blank" rel="noreferrer">IBM Technology Zone Help</a> regarding issues with reserving and provisioning Tech Zone environments.<br/>• Contact <a href="https://ibm-cloud.slack.com/archives/C0216F39ACU" target="_blank" rel="noreferrer">#platinumdemos-automation-support</a> regarding issues with setting up and running this demo. |

<details markdown="1">

<summary>1 - Access the demo environment (IBMers)</summary>

This demo is available on several sales demonstration and enablement tenants (demo instances). For new watsonx Orchestrate users, please request access by submitting a <a href="https://ibm.biz/OrchestrateRequestEnv" target="_blank" rel="noreferrer">request here</a>. You will receive an email once you have been onboarded onto a suitable tenant, but please allow 48 hours for your request to be processed.<br/> 

Based on your role and requirements, you will be onboarded onto a sales demonstration tenant or an enablement tenant. Enablement tenants provide short-term access (two week maximum) for enablement purposes. 

Once you have received your onboarding email use your IBM email to log in <a href="https://dl.watson-orchestrate.ibm.com/home" target="_blank" rel="noreferrer">here</a>. <br/>

**Cannot find the demo or skills?**

If you are an existing watsonx Orchestrate user but you cannot see the skills needed to run the demo(they are represented as cards at the bottom of the watsonx screen), please ensure you are in the **Team skills** view. When you log into watsonx Orchestrate, the default view is **Personal skills**. To run the demo, change the view to **Team skills**.<br/><img src="images/prep-1-2-teamskills.jpg" width="600" /> <br/>

If you are an existing watsonx Orchestrate user and still cannot see the skills used in the demo, please request access to a suitable tenant by submitting a <a href="https://ibm.biz/OrchestrateRequestEnv" target="_blank" rel="noreferrer">request here</a>. You will receive an email once you have been onboarded onto a suitable tenant, but please allow 48 hours for your request to be processed.<br/> 

Users with access to multiple tenants (demo environments) should ensure they select a tenant that has the demonstration installed. Please use the <a href="https://ibm-cloud.slack.com/archives/C0216F39ACU" target="_blank" rel="noreferrer">#platinumdemos-automation-support</a> Slack channel if you require assistance. 
<br/> 

</details>

<p/>

<details markdown="1">

<summary>2 - Access the demo environment (Business Partners)</summary>

If you do not have access to a tenant, you can request access by submitting a <a href="https://ibm.biz/OrchestrateRequestEnv" target="_blank" rel="noreferrer">request here</a>. You will receive an email once you have been onboarded onto a suitable tenant, but please allow 48 hours for your request to be processed.<br/><br/>

Once you have received your onboarding email, use your IBM ID to log in <a href="https://dl.watson-orchestrate.ibm.com/home" target="_blank" rel="noreferrer">here</a>.<br/>

</details>

<p/>

<details markdown="1">

<summary>3 - Add custom Salesforce skill</summary>

1. Click the **Team skills** drop-down menu (1) and click **Personal skills** (2). <br/> <img src="images/Prep-1-1.png" width="500" /><br/>

2. Click the **Add skills from the catalog** tile. <br/> <img src="images/Prep-1-2.png" width="500" /><br/>

3. Search for '**life**' in the search panel. <br/> <img src="images/Prep-1-3.jpg" width="800" /><br/>

4. The list of apps is filtered to only show apps that contain skills containing the word 'life.' Click the **Salesforce – Get customers with recent life changes** card. <br/> <img src="images/Prep-1-4.jpg" width="800" /><br/>

5. Click **Add skill +** (1). Click **Connect app** (2). <br/> <img src="images/Prep-1-5.jpg" width="800" /><br/>

6. Use the following credentials: <br/><br/> • **Client ID** (1): 3MVG9HB6vm3GZZR_fBoKSxSomjQ8ZaShg9mWyjw2pJak55hcL8KGtUjjkooS7wpLD25QraIBxop4ThrTPK237 <br/> • **Client Secret** (2): 34CB8CCE1E4495C0CAE6A921A5FC7D17CC6CE614152175D20F5B00F8B250626C <br/><br/> Click **Connect app** (3). <br/> <img src="images/Prep-1-6.jpg" width="800" /><br/>

7. Click the **menu slider** icon. <br/> <img src="images/Prep-1-7.jpg" width="500" /><br/>

8. Click **Home**. <br/> <img src="images/Prep-1-8.jpg" width="500" /><br/>

9. Test the skill works correctly by clicking the skill tile. <br/> <img src="images/Prep-1-9.jpg" width="500" /><br/>

10. A table should be shown containing the data from Salesforce. <br/> <img src="images/Prep-1-10.jpg" width="500" /><br/>
   
</details>

<p/>

<details markdown="1">

<summary>4 - Add product upsell skill</summary>

The next personal skill to add will be based on a decision model imported into Automation Builder.

1. Click **Add skills from the catalog**. <br/> <img src="images/Prep-2-1.jpg" width="700" /><br/>

2. Search for '**Product**' in the search panel. <br/> <img src="images/Prep-2-2.jpg" width="700" /><br/>

3. Click **Product Upsell**. <br/> <img src="images/Prep-2-3.png" width="700" /><br/>

4. Click **Add skill +**. <br/> <img src="images/Prep-2-4.png" width="500" /><br/>

</details>

<p/>

<details markdown="1">

<summary>5 - Update the Salesforce OpenAPI file</summary>

<inline-notification text="The OpenAPI file must be updated before it can be used to import a new skill. This is necessary as Orchestrate uses  a few attributes as the unique ID for the skill and this skill has already been imported as a team skill.<br/> We recommend using Microsoft VSCode editor to edit the OpenAPI file."></inline-notification>

1. Download the OpenAPI file: <a href="files/GetSalesforceCustomers.json" target="_blank" rel="noreferrer">GetSalesforceCustomers.json</a><br/><br/>
2. In a multi-user environment, we must provide unique values for the API. There are five attributes to update: **title** and **description** in the "info" section (near the top of the file), and **description**, **summary** and **operationId** in the "paths" section (near the bottom of the file). <br/> <img src="images/Prep-3-1-0.png" width="800" /><br/> <img src="images/Prep-3-1.png" width="800" /><br/><br/> Add your initials and date to the five attributes. Your changes should look as below:<br/><img src="images/Prep-3-1-1.png" width="800" /><br/><img src="images/Prep-3-1-2.png" width="800" /></br/>

</details>

<p/>

### **PREPARATION REQUIRED TO GIVE THIS DEMO AGAIN**

### **AFTER EACH DEMO**

<details markdown="1">

<summary>Skill cleanup</summary>

The watsonx Orchestrate environment used for the demo is shared by many users. After completing your demo, please take a few minutes to remove any skills or automations you created during the demo. Then, also remove the personal skills created during the demo preparation. Finally, remove the decision automation that was imported.

1. Click the **menu slider** icon and select **Skills**. Use the search panel to find the skill flow that was created in the demo. In the example demo, this was created as '**GB Upsell Skill**' (it is listed below as a composite skill). Expand the skill details to confirm you are the author. Click the corresponding **ellipsis** icon to the right of the screen. Click **Delete this skill**. <br/> <img src="images/Prep-6-1.png" width="800" /><br/>

2. Remove the skill that was created using an OpenAPI file. During the preparation for this skill import, it was recommended to add a unique ID to the description attribute in the OpenAPI file. (In the example, 'GB081123' was added to the description attribute.) Use your unique ID to find the skill. Expand the skill details to confirm you are the author. Click the **ellipsis** icon and click **Delete this skill**. <br/> <img src="images/Prep-6-2.png" width="800" /><br/>

</details>

Click [here](demo-script) to go to the **Demo script** on the next tab.