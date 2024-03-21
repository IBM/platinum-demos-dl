---
title: Predictive decisioning <br/> 300-level live demo
layout: preparation
banner: images/Predictive-Decisioning-300-Prep-GitHub-banner-12-15-21.jpg
---


| DEMO OVERVIEW | |
| :---         | :--- |
| **Scenario overview** | This demo shows how the IBM Cloud Pak for Business Automation integrates machine learning to improve decisions. To illustrate this, a company’s customer retention offer process is automated. |
| **Demo products** | Cloud Pak for Business Automation, Cloud Pak for Data (Machine learning capabilities) |
| **Demo capabilities** | Decision management; Machine learning |
| **Sales guidance** | Download the sales guidance document <a href="./files/Predictive Decisioning Platinum Demo - Sales guidance.pdf" target="_blank" rel="noreferrer">here</a>. |
| **Demo intro slides** | Download the Introduction and Overview slides <a href="./files/Predictive Decisioning Platinum Demo - Intro deck.pptx" target="_blank" rel="noreferrer">here</a>. This is a short deck of customer-facing slides that sets the context for the demo. |
| **Demo script** | A complete demo script is on the second tab above. You can download a printer-ready PDF of the demo script <a href="./files/Predictive Decisioning Platinum Demo - PDF script.pdf" target="_blank" rel="noreferrer">here</a>. <br/><br/> This demo script has multiple tasks that each have multiple steps. In each step, you have the details about what you need to do (**Actions**), what you can say while delivering this demo step (**Narration**), and screenshots of what you will see.<br/><br/>This demo script is a suggestion, and you are welcome to customize based on your sales opportunity. Most importantly, practice this demo in advance. If the demo seems easy for you to execute, the customer will focus on the content. If it seems difficult for you to execute, the customer will focus on your delivery. |
| **Demo downloads** | • <a href="./files/Retention Policy.pdf" target="_blank" rel="noreferrer">SkyTalk’s Retention offer document.pdf</a> <br/>• <a href="./files/SkyTalk customer loyalty data.csv" target="_blank" rel="noreferrer">SkyTalk customer loyalty data.csv</a> <br/>• <a href="./files/SkyTalk customer value data.csv" target="_blank" rel="noreferrer">SkyTalk customer value data.csv</a> <br/>• <a href="./files/SkyTalk_call_center_application_23.0.2.twx" target="_blank" rel="noreferrer">SkyTalk_call_center_application_23.0.2.twx</a> <br/>• <a href="./files/SkyTalk-customer-retention_23.0.2.zip" target="_blank" rel="noreferrer">SkyTalk-customer-retention_23.0.2.zip</a> |
| **Sales enablement video** | View the enablement video  <a href="https://ibm.box.com/s/mzlmipw8gux5xnaeokjgvko10vxrsdkl" target="_blank" rel="noreferrer">here</a>. This video is for enablement purposes only (IBMers and Business Partners) and is not customer-ready. |
| **Required versions** | Cloud Pak for Business Automation V23.0.2, Cloud Pak for Data 4.0 <br/> |
| **How to get support** | • Open a support case at <a href="https://techzone.ibm.com/help" target="_blank" rel="noreferrer">IBM Technology Zone Help</a> regarding issues with reserving and provisioning Tech Zone environments.<br/>• IBMers, contact <a href="https://ibm.enterprise.slack.com/archives/C06HT5PHLN9" target="_blank" rel="noreferrer">#ba-techlcd-support</a>  regarding issues with setting up and running this demo. |

<span id="top"></span>

This platinum demo uses machine learning resources that are subject to a quota. It is critical to stop depleting your machine learning quota by following the ‘**After each demo**’ steps detailed in this preparation guide unless you are practicing or presenting this demo.

The ‘**Preparation required to give this demo again**’ section details how to re-deploy the required machine learning service prior to your next demo.

The five components of the demo:<br/><br/>

<img src="images/Prep267.png" width="800" />

## **MANAGING YOUR WATSON STUDIO FREE SUBSCRIPTION**

This demonstration requires Watson Studio and a Watson Machine Learning subscription. If you don’t have a paid subscription, you can use a free Lite version (which has a limited quota). This preparation guide explains how to provision a Watson Studio account.

The Lite version entitles you to **10 free CUH** (capacity units) per calendar month. The quota resets on the first of each month.

The 10 CHU allows for **3 to 5 hours of usage**, which is measured as the total time Watson Machine Learning is deployed. To stop the clock, you must undeploy the 2 ML services (see the ‘After each demo’).

Assuming you undeploy after each time you give or practice the demo, we estimate that you can do the demo **three to five times per month** without exceeding the free Watson Machine Learning limit. If you leave the two machine learning services deployed overnight, it will consume all your monthly limit in just 3 to 5 hours of time.

## **DEMO INSTALLATION AND SETUP**
<span id="importFlow"></span>
<details markdown="1">

<summary>1 - Provision an OpenShift environment and deploy Cloud Pak for Business Automation</summary>

To run this demonstration, you will need an OpenShift environment with Cloud Pak
for Business Automation 23.0.2 installed. We will use IBM Operational Decision
Manager on prem version contained in this installation. <br/> <inline-notification text="Note: If you want to use your ODM hosted on a SaaS tenant, just contact your SaaS administrator to get a user and password to connect your RES in Basic Authentication. Go directly to Step 3: Download the installation files."></inline-notification>

1. Visit the <a href="https://techzone.ibm.com/collection/tech-zone-certified-base-images/journey-pre-installed-software" target="_blank" rel="noreferrer">TechZone environment provisioning</a> page. <br/><br/>

2. Click the **CP4BA 23.0.x - Multi-Pattern Starter** tile. <br/> <img src="images/Prep-1-2-2.png" width="800" /><br/>

3. Select **Reserve now** tile. <br/> <img src="images/Prep-1-2-3.png" width="800" /><br/>

4. Select **Practice / Self-Education** <br/> <img src="images/Prep-1-2-4.png" width="800" /><br/>

5. Enter a **Purpose description** <br/> <img src="images/Prep-1-2-5.png" width="800" /><br/>

6. Select your **Preferred Geography** <br/> <img src="images/Prep-1-2-6.png" width="800" /><br/>

7. Select  **'5''** as **'Worker Node Couunt'**<br/> <img src="images/Prep-1-2-7.png" width="800" /><br/>

8. Select **’16 vCPU x 64GB – 100GB ephemeral storage’** as the **Starter service** (1) in the **Worker Node Flavor** <br/> <img src="images/Prep-1-2-8.png" width="800" /><br/>

9. Read and agree to **IBM Technology Zone's Terms and Conditions and End User Security Policies** (1). Click **Submit** (2). <br/> <img src="images/Prep-1-2-9.png" width="800" /><br/>

10. Check that the request was correctly submitted, and wait for the confirmation emails. <br/> <img src="images/Prep-1-2-10.png" width="800" /><br/>

**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>2 - Validate your environment and bookmark your IDs and URLs</summary>
<br/>
After 4-5 hours, your Cloud Pak for Business Automation (CP4BA) should be ready. After requesting your CP4BA, you will receive a series of emails from IBM Technology Zone regarding the progress of your request.

1. Check for an email with the subject **Reservation Ready on IBM Technology Zone** (1). Click **View My Reservations** (2) <br/> <img src="images/Prep-2-1-1.png" width="800" /><br/>

2. Copy paste your **Kubeadmin / Passwords** in your notebook <br/> <img src="images/Prep-2-1-2.png" width="800" /><br/>

3. Click your reservation tile. <br/> <img src="images/Prep-2-1-3.png" width="800" /><br/> <inline-notification text="Your reservation status should be <strong>Ready</strong>"></inline-notification> 

4. Click the **Open your IBM Cloud environment**. <br/> <img src="images/Prep-2-1-4.png" width="800" /><br/>

1. Log in to your OpenShift console using the credentials provided during section 1 above.<br/><br/>

6. Expand the **Workloads** (1) and click **ConfigMaps** (2). <img src="images/Prep-2-6.png" width="800" /><br/>

7. Expand the **projects** menu (1) and click **cp4ba-starter** (2).<img src="images/Prep-2-7.png" width="800" /><br/>

8. Type '**access**' (1). Check that the **icp4adeploy-cp4ba-access-info** config map is present. <img src="images/Prep-2-8.png" width="800" /><inline-notification text="If the file is not listed, wait five more minutes for the CP4BA deployment to be completed"></inline-notification>

9. Click **icp4adeploy-cp4ba-access-info**. <img src="images/Prep-2-9.png" width="800" /><br/>

10. Scroll down (1) and check that all the ADS access information is displayed. ADS is the last element to install, so your CP4BA setup is completed once this info displays. <br/><img src="images/Prep-2-10.png" width="800" /><br/>

11. Copy the **CP4admin username** and **password** used to log in to the various CP4BA components into a note to access later. <img src="images/Prep-2-11.png" width="800" /><br/>

12. Copy the **URL** needed to access the various products required in this demonstration into a note to access later.<img src="images/Prep-2-12.png" width="800" /><br/>

**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>3 - Create and configure a GitHub repository </summary>
<br/>
A GitHub repository is required to manage decision projects in ADS. You must create a personal Git repository. You can use for example https://github.com and create your own account. IBMers can use the IBM enterprise git on https://github.ibm.com.
<br/>
After logging into GitHub:
<br/>
1. Click **New** in the repository section.<img src="images/Prep10.png" width="800" /><br/>
2. Enter ‘**SkyTalk retention DS**’ (1) in the **Repository name** field. Click **Create repository** (2).<br/><img src="images/Prep11.png" width="800" /><br/>
3. Bookmark the repository URL (to configure ADS in a future step).<br/><img src="images/Prep12.png" width="800" /><br/>
4. Click your **profile** icon (1), then select **Settings** (2).<br/><img src="images/Prep13.png" width="800" /><br/>
5. Click **Developer settings**.<br/><img src="images/Prep14.png" width="800" /><br/>
6. Expand **Personal access tokens** and click **Tokens (classic)**.<br/><img src="images/Prep15.png" width="800" /><br/>
7. Click **Generate new token**.<br/><img src="images/Prep16.png" width="800" /><br/>
8. Enter **'ADS Platinum demo 23.0.2'** in the **Note** (1) and check **repo** (2).<br/><img src="images/Prep-3-8.png" width="800" /><br/>
9. Scroll down and click **Generate token**.<br/><img src="images/Prep18.png" width="800" /><br/>
10. Copy the **Personal access token** ID (it will be used in ADS).<br/><img src="images/Prep19.png" width="800" /><br/>
11. Expand your profile (1) and copy your **username** (it will be used in ADS).<br/><img src="images/Username.png" width="800" /><br/>

**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>4 - Create and set up a Watson Studio account </summary>
1. Go to <a href="http://cloud.ibm.com" target="_blank" rel="noreferrer">IBM Cloud</a>.<br/>
2. Enter your **IBM ID**. If you do not have one, create a new one.<br/>
3. Ensure you are in your own Cloud Pak for Data account instance (1). Click **Create resource** (2).
<br/><img src="images/Prep20.png" width="800" /><br/>
4. If prompted, click **Go** in the **Internal Paid Account** column.<br/><img src="images/Prep268.png" width="800" /><br/>
5. Type **'watson'** (1) in the search field and then select **Watson Studio** (2).
<br/><img src="images/Prep21.png" width="800" /><br/>
6. Select the **Lite** plan (1) and a **location** (2). Read and accept **license agreements** (3). Click **Create** (4).
<br/><img src="images/Prep22.png" width="800" /><br/>
7. Return to **IBM Cloud**.
<br/><img src="images/Prep23.png" width="800" /><br/>
8. Click **Create resource**.<br/><img src="images/Prep24.png" width="800" /><br/>
9. Type **'machine'** (1) in the search field and then select **Watson Machine Learning** (2).
<br/><img src="images/Prep25.png" width="800" /><br/>
10. Select the **Lite** plan (1) and a **location** (2). Read and accept **license agreements** (3). Click **Create** (4).
<br/><img src="images/Prep26.png" width="800" /><br/>
11. Return to **IBM Cloud**.
<br/><img src="images/Prep27.png" width="800" /><br/>
12.	Click **Create resource**.
<br/><img src="images/Prep28.png" width="800" /><br/>
13. Type **'Object'** (1) in the search field and then select **Object Storage** (2).
<br/><img src="images/Prep29.png" width="800" /><br/>
14. Select **IBM Cloud** (1). Choose the **Lite** plan (2) and click **Create** (3).
<br/><img src="images/Prep30.png" width="800" /><br/>
15. Expand the **top menu** (1) and then select **Resource list** (2).
<br/><img src="images/Prep31.png" width="800" /><br/>
16. The new services should appear. Click **Watson Studio-2d**.
<br/><img src="images/Prep32.png" width="800" /><br/>
17. Click **Launch in IBM Cloud Pak for Data**.
<br/><img src="images/Prep33.png" width="800" /><br/>
18. Click **+** next to **Deployments**.
<br/><img src="images/Prep34.png" width="800" /><br/>
19. Name the production space **'SkyTalk production space'** (1). Select **Cloud Object Storage-xx** as the **storage service** (2). Select your **Machine Learning-xx** (3) as the machine learning service. Click **Create** (4).<br/><img src="images/Prep35.png" width="800" /><br/>
20.	Click **Close**.<br/><img src="images/Prep36.png" width="800" /><br/>
21. Click the **IBM Watson Studio** logo on the left side of the toolbar to return to the home page.<br/><img src="images/Prep37.png" width="800" /><br/>

**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>5 - Set up two machine learning models </summary>
The Watson Studio environment is completely set up. The three services (Watson Studio, ML, and Storage) are ready, and the deployment environment is set up. Now let’s create the two prediction services using AutoAI in Watson Studio.
<br/>
Ensure you have downloaded these two data files prior to starting this step:
<br/>
<a href="./files/SkyTalk customer loyalty data.csv" target="_blank" rel="noreferrer">SkyTalk customer loyalty data.csv</a><br/>
<a href="./files/SkyTalk customer value data.csv" target="_blank" rel="noreferrer">SkyTalk customer value data.csv</a>
<br/><br/>
1. Click **+** next to **Projects**.
<br/><img src="images/Prep38.png" width="800" /><br/>
2. Select **Create an empty project**.
<br/><img src="images/Prep39.png" width="800" /><br/>
3. Name the project **'SkyTalk customer retention'** (1) and click **Create** (2).<br/>
<br/><img src="images/Prep40.png" width="800" /><br/>
4. Click the **Assets** tab.<br/>
<br/><img src="images/Prep41.png" width="800" /><br/>
5. Click **New asset +**.
<br/><img src="images/Prep42.png" width="800" /> <br/>
6. Select **AutoAI**.
<br/><img src="images/Prep43.png" width="800" /> <br/>
7. Name the AutoAI experiment **'SkyTalk churn prediction'** (1) and click **Associate a Machine Learning service instance** (2).
<br/><img src="images/Prep44.png" width="800" /><br/>
8. Select the **Machine learning-xx** (1) service. Click **Associate** (2).
<br/><img src="images/Prep45.png" width="800" /> <br/>
9. Click **Reload**.
<br/><img src="images/Prep46.png" width="800" /> <br/>
10. Click **Create**.
<br/><img src="images/Prep47.png" width="800" /> <br/>
11. Click **Browse**.
<br/><img src="images/Prep48.png" width="800" /> <br/>
12. Select the **SkyTalk customer loyalty data.csv** file (1) and click **Open** (2).
<br/><img src="images/Prep49.png" width="800" /> <br/>
13. When prompted **‘Create a time series forecast?'**, click **No**.
<br/><img src="images/Prep50.png" width="800" /> <br/>
14. When prompted **'What do you want to predict?'**, select **CHURN**.
<br/><img src="images/Prep52.png" width="800" /><br/>
15. Click **Run experiment**.
<br/><img src="images/Prep53.png" width="800" /> <br/>
16. The tool will create 8 pipelines, which will take approximately two minutes.
<br/><img src="images/Prep54.png" width="800" /> <br/>
17.	Scroll down to the pipeline marked with a star in the **Pipeline leaderboard** list and click **Save as** in the corresponding row.
<br/><img src="images/Prep55.png" width="800" /> <br/>
18. Select **Model** (1) and click **Create** (2).
<br/><img src="images/Prep56.png" width="800" /> <br/>
19. A **Saved model successfully** confirmation message appears.
<br/><img src="images/Prep57.png" width="500" /><br/>
20. Return to the project view by clicking **SkyTalk customer retention** in the breadcrumb navigation.
<br/><img src="images/Prep58.png" width="800" /><br/>
21. Click **New asset +**.
<br/><img src="images/Prep59.png" width="800" /><br/>
22.	Repeat steps 6 – 21 to create another model to predict Skytalk’s customer lifetime value.<br/>
• When repeating step 7, name the AutoAI experiment **‘SkyTalk lifetime value prediction’**. <br/>
• When repeating step 12, select the **SkyTalk customer value data** (2) file.<br/>
• When repeating step 14, select the **Lifetimevalue**.
<br/>
23.	After saving the starred pipeline as the **Skytalk lifetime value prediction** model, return to the project view by clicking **SkyTalk customer retention** in the breadcrumb menu.<br/><img src="images/Prep61.png" width="800" /><br/>
The two models display and are ready to be published in the deployment space.
<br/><img src="images/Prep62.png" width="800" /><br/>
24.	Hover the mouse over the first model and click **Promote to space**.
<br/><img src="images/Prep63.png" width="800" /><br/>
25.	Choose the **SkyTalk production space** (1) as the **Target space** and click **Promote** (2).
<br/><img src="images/Prep64.png" width="800" /><br/>
26.	Repeat steps 4.24 and 4.25 to promote the second model.
<br/>
27.	Return to the IBM Watson Studio home page then click **SkyTalk production space** in the deployment space section.
<br/><img src="images/Prep65.png" width="800" /><br/>
28.	Select the **Assets** tab.
<br/><img src="images/Prep66.png" width="800" /><br/>
29.	The **Assets** tab displays. The two Machine learning services are ready to be deployed.
<br/><img src="images/Prep67.png" width="800" /><br/>

**[Go to top](#top)**

</details>

<span id="step4"></span>

<details markdown="1">

<summary>6 - Deploy the ML models</summary>
<inline-notification text="Any time your ML services are deployed, your Machine Learning Lite subscription quota is consumed. To avoid running out of Watson ML quota, undeploy your ML services whenever you are not practicing or giving this demo."></inline-notification>
<br/>
The **Reset the demo to its beginning state** step on this page below contains the process to undeploy the services and stop the billing process.
<br/>
Redeploy your ML services approximately 15 minutes prior to practicing or giving this demo.
<br/>
1. From the Watson Studio environment, select the **SkyTalk production space** deployment space.
<br/><img src="images/Prep68.png" width="800" /><br/>
2. Select the **Assets** tab.
<br/><img src="images/Prep69.png" width="800" /><br/>
3. Deploy the **Skytalk churn prediction** by hovering your mouse over the right side of the corresponding row, clicking the rocket icon that appears, and clicking **Deploy**.
<br/><img src="images/Prep70.png" width="800" /><br/>
4. Select **Online** (1), name the deployment **'churn'** (2), and click **Create** (3).
<br/><img src="images/Prep71.png" width="800" /><br/>
5. Return to the **SkyTalk production space** using the breadcrumb menu and deploy the **Skytalk lifetime value prediction** by hovering your mouse over the right side of the corresponding row, clicking the rocket icon that appears, and clicking **Deploy**.
<br/><img src="images/Prep72.png" width="800" /><br/>
6. Select **Online** (1), name the deployment **'Lifetime value'** (2), and click **Create** (3).
<br/><img src="images/Prep73.png" width="800" /><br/>
7. Return to the **SkyTalk production space** using the breadcrumb menu and click the **Deployments** tab. Ensure the two services are deployed.
<br/><img src="images/Prep74.png" width="800" /><br/>

**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>7 - Get the credentials to set up the ML provider</summary>
This section explains how to get the credentials to set up the machine learning provider in ADS.
<br/>
1. In the **Deployments - SkyTalk production space**, select the **Deployments** tab (1) and click **churn** (2).
<br/><img src="images/Prep75.png" width="800" /> <br/>
2. Copy the first portion of the **Endpoint** URL path (the blue hightlighted section in the screenshot) and save it for the upcoming ML provider configuration.
<br/><img src="images/Prep76.png" width="800" /> <br/>
3. Click **SkyTalk production space** in the breadcrumb menu.
<br/><img src="images/Prep77.png" width="800" /><br/>
4. Select the **Manage** tab.
<br/><img src="images/Prep78.png" width="800" /><br/>
5. Copy the deployment **Space GUID** and save it for the upcoming ML provider configuration step.
<br/><img src="images/Prep79.png" width="800" /> <br/>
6. Log out and return to the IBM Cloud environment at  <a href="http://cloud.ibm.com" target="_blank" rel="noreferrer">cloud.ibm.com </a>. Make sure you are in your personal Cloud Pak for Data instance.
<br/><img src="images/Prep80.png" width="800" /> <br/>
7. Click the **Manage** tab and select **Access (IAM)**.
<br/><img src="images/Prep81.png" width="800" /> <br/>
8. Click **API keys** (1) and then click **Create +** (2).
<br/><img src="images/Prep82.png" width="800" /> <br/>
9. Name the key **'MY_API_Key'** (1) and click **Create** (2).
<br/><img src="images/Prep83.png" width="500" /><br/>
10.	Click **Download** to save the **API key file** for the upcoming ML provider configuration.
<br/><img src="images/Prep84.png" width="800" /><br/>

**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>8 - Open Automation Decision Services (ADS) and import the ADS demo project </summary>
Prior to performing this step, make sure you have downloaded the <a href="./files/SkyTalk-customer-retention_23.0.2.zip" target="_blank" rel="noreferrer">SkyTalk-customer-retention_23.0.2.zip</a> file. This file is required to set up the ADS decision service.
<br/>
1. Access the Cloud Pak for Business Automation using the bookmark saved in step 2. Select **Enterprise LDAP** in the **Log in with** drop down menu (1). Enter **‘cp4admin’** as the **Username** and the **Password** (2) from your note. Click **Log in** (3).<br/><img src="images/Prep269.png" width="800" /><br/>
2. Expand the **top menu** (1) and click **Business automations** (2) under **Design**.
<br/><img src="images/Prep85.png" width="800" /><br/>
3. Pass through the privacy warning messages by clicking **advanced** and then the **'proceed...'** link.<br/><br/>
4. Under **Business automations**, click **Create** (1) and select **Decision automations** (2).
<br/><img src="images/Prep86.png" width="800" /><br/>
5. Name the automation **'Customer retention'** (1) and then click **Create** (2).
<br/><img src="images/Prep87.png" width="800" /><br/>
6. Accept any privacy checks that may appear.
<br/><img src="images/Prep88.png" width="500" /><br/>
7. Close any guided tour views.<br/><br/>
8. Click **New decision**.
<br/><img src="images/Prep-new-decision.png" width="800" /><br/>
9. Click **Import decision service**.
<br/><img src="images/Prep-click-import-ds.png" width="800" /><br/>
10. Click **Browse**.
<br/><img src="images/Prep-click-browse.png" width="800" /><br/>
11. Select the <a href="./files/SkyTalk-customer-retention_23.0.2.zip" target="_blank" rel="noreferrer">SkyTalk-customer-retention_23.0.2.zip</a> file (1) and click **Open** (2).
<br/><img src="images/Prep-8-11.png" width="800" /><br/>
12. Click **Import**.
<br/><img src="images/Prep-click-import.png" width="800" /><br/>
13. Configure the ADS environment by clicking the **Settings** icon.
<br/><img src="images/Prep-settings-icon.png" width="800" /><br/>
14. In the **Remote Git repositories** tab, paste the git **Repository URL** (1) from step 2.3. Select **Create or update credentials for the decision automation** (2).
<br/><img src="images/RepositoryURL.png" width="800" /><br/>
15. Click **Username & password** (1), enter your Git username in the **Username** field, and enter the Git **Personal access token (API key)** from step 2.10 in the **Password** field (3). Click **Connect** (4).
<br/><img src="images/Credentials.png" width="800" /><br/>
16. Ensure that the **Remote Git repository** status is successfully connected.<br/><img src="images/Prep94.png" width="800" /><br/>To perform the following steps, your two machine learning services must be deployed in the Watson Studio deployment environment.
17.	Click the **Machine learning providers** tab to configure the machine learning provider.
<br/><img src="images/Prep95.png" width="800" /><br/>
18. Click **New +**.
<br/><img src="images/Prep96.png" width="800" /><br/>
19. Select the **Watson ML** (1) machine provider type and name the ML provider **'SkyTalk ML provider'** (2). Enter the **URL** (3) and **Space ID** (4) from step 7.5 and scroll down.<br/><br/>NOTE: The **Space ID** is the **Space GUID**.
<br/><img src="images/MLprovider.png" width="800" /><br/>
20. Enter the **API key** (1) from step 7.5, and click **Test connection** (2).<br/><br/>NOTE: The **Space ID** is the **Space GUID**.
<br/><img src="images/TestConnection.png" width="800" /><br/>
21. If the connection is successful, click **Save**.
<br/><img src="images/Prep98.png" width="800" /><br/>
22. Click **Customer retention** in the breadcrumb menu.
<br/><img src="images/Prep99.png" width="800" /><br/>

**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>9 - Update the decision model with the deployed ML models</summary>
1. Click the **Retention ML** tile.
<br/><img src="images/Prep100.png" width="800" /><br/>
2. Click the **Customer Churn** model on the **Models** tab.
<br/><img src="images/Prep101.png" width="800" /><br/>
3. Click **Configure**.
<br/><img src="images/Prep102.png" width="800" /><br/>
4. Select **Remote machine learning model** (1) and click **Next** (2).
<br/><img src="images/Prep103.png" width="800" /><br/>
5. Select **SkyTalk ML provider** as the **Machine learning provider**.
<br/><img src="images/Prep104.png" width="800" /><br/>
6. Expand the **SkyTalk churn prediction model** (1), select the **churn** deployment (2), and click **Next** (3).
<br/><img src="images/Prep105.png" width="800" /><br/>
7. Click **Next**.
<br/><img src="images/Prep106.png" width="800" />
8. Click **Run** to test the invocation.
<br/><img src="images/Prep107.png" width="800" /><br/>
9. If the test succeeds, click **Next**.
<br/><img src="images/Prep108.png" width="800" /><br/>
10. Click **Generate from test output**.
<br/><img src="images/Prep109.png" width="800" /><br/>
11. Click **OK**.
<br/><img src="images/Prep110.png" width="800" /><br/>
12. Click **Apply**.
<br/><img src="images/Prep111.png" width="800" /><br/>
13. Click **Retention ML** in the breadcrumb menu.
<br/><img src="images/Prep112.png" width="800" /><br/>
14. Click **Customer Lifetime Value** and repeat steps 3 - 13 to configure the model. When repeating step 6, expand the **Skytalk lifetime value prediction** ML model and select **Customer lifetime value**.
<br/><img src="images/Prep113.png" width="800" /><br/>
15. Click the **Retention offer** model.
<br/><img src="images/Prep114.png" width="800" /><br/>
16. Select the **Run** tab.
<br/><img src="images/Prep115.png" width="800" /><br/>
17. Select the **High value profile** test file (1) and click **Run** (2). <br/><br/>The retention offer **Result** should display.  Click **Run** again if you get a timeout error the first time.
<br/><img src="images/Prep116.png" width="800" /><br/>
Your result should match the screenshot below.<br/><img src="images/Prep117.png" width="800" /><br/>

**[Go to top](#top)**

</details>

<span id="step10"></span>

<details markdown="1">

<summary>10 - Deploy the decision service</summary>
1. Click **Customer retention** in the breadcrumb menu.
<br/><img src="images/Prep-10-1.png" width="800" /><br/>
2. Select the **Share changes** tab.
<br/><img src="images/Prep-10-2.png" width="800" /><br/>
3. Click the **share all changes** box (1) and click **Share** (2).
<br/><img src="images/Prep-10-3.png" width="800" /><br/>
4. Click **Share** to push the updates to the Git repository.
<br/><img src="images/Prep-10-4.png" width="800" /><br/>
5. Select the **View history** tab.
<br/><img src="images/Prep-10-5.png" width="800" /><br/>
6. Refresh the page and then click **Version +** in the latest shared history.
<br/><img src="images/Prep-10-6.png" width="800" /><br/>
7. Enter version **'1.0.0'** (1) in the **Name** field and click **Create** (2).
<br/><img src="images/Prep-10-7.png" width="800" /><br/>
8. Click the **Deploy** tab.
<br/><img src="images/Prep-10-8.png" width="800" /><br/>
9. Expand the most recently created version **(1.0.0)** (1) and click **Deploy** (2) in the **Retention ML** row.
<br/><img src="images/Prep-10-9.png" width="800" /><br/>
10. Click **Deploy** to confirm.
<br/><img src="images/Prep-10-10.png" width="800" /><br/>
11. Wait for the deployment to finish (1). Click **Business Automations** (2) in the breadcrumb menu.
<br/><img src="images/Prep-10-11.png" width="800" /><br/>
12.	Select **Decision** (1) and then click the **Customer retention** tile (2).<br/><br/><inline-notification text=" Do not select <strong>Open</strong> on the tile."></inline-notification><br/><img src="images/Prep129.png" width="800" /><br/>
13.	The most recently deployed service displays. Click the **three dots** icon (1) and then select **Publish** (2).
<br/><img src="images/Prep130.png" width="800" /><br/>
14. Click **Publish**.
<br/><img src="images/Prep131.png" width="800" /><br/><inline-notification text="If the publish fails, wait for 5 minutes and try again. Some deployment operations may still be occurring in background."></inline-notification> 
15. Ensure the service appears as **Published**.
<br/><img src="images/Prep132.png" width="800" /><br/>

**[Go to top](#top)**

</details>

<span id="step11"></span>

<details markdown="1">

<summary>11 - Configure Application Designer and import the client application</summary>
Prior to performing this step, make sure you have downloaded the <a href="./files/SkyTalk_call_center_application_23.0.2.twx" target="_blank" rel="noreferrer"> SkyTalk_call_center_application_23.0.2.twx</a> archive file. This file is required to set up the ADS decision service.
<br/>

1. Expand the **top menu** (1), click **Design** (2), and then click **Business applications** (3).<br/><img src="images/Prep-11-1.png" width="800" /><br/>

2. Click **Import**. <br/><img src="images/Prep-11-2.png" width="800" /><br/>

3. Click the **upload link**. <br/><img src="images/Prep-11-3.png" width="800" /><br/>

4. Select the **SkyTalk_call_center_application_23.0.2.twx** file (1) and then click **Open** (2). <br/><img src="images/Prep-11-4.png" width="800" /><br/>

5. Click **Import**. <br/><img src="images/Prep-11-5.png" width="800" /><br/>

6. Click **Done**.<br/><img src="images/Prep-11-6.png" width="800" /><br/>

7. After the import, hover the mouse over the **SkyTalk call center Application** tile and click **Open**.<br/><img src="images/Prep-11-7.png" width="800" /><br/>

8. Click the **gear** icon. <br/><img src="images/Prep138.png" width="800" /><br/>

9. Set the **View mode** (1) to **Advanced**. Click **Save** (2). <br/><img src="images/Prep139.png" width="800" /><br/>

10. Refresh the page and ensure the **Overview**, **Diagram**, and **Variables** tabs are visible. <br/><img src="images/Prep-11-10.png" width="800" /><br/>

11. Click the **gear** icon on the left-hand side ribbon. <br/><img src="images/Prep-11-11.png" width="800" /><br/>

12. Click **Action and services** (1), right-click **rentention_ml** (2) and then click **Delete** (3). <br/><img src="images/Prep-11-12.png" width="800" /><br/>

13. Click **Yes** to confirm.  <br/><img src="images/Prep143.png" width="800" /><br/>

14. Click the **Diagram** tab.<br/><img src="images/Prep-11-14.png" width="800" /><br/>

15. Select the **Call skytalk_retention_ds** node (1) and then click the **Implementation** tab (2) below the diagram. <br/><img src="images/Prep-11-15.png" width="800" /><br/>

16. Click **New…** <br/><img src="images/Prep-11-16.png" width="800" /><br/>

17. Click **retention_ml Decision** (1), select the most recent version (2) as the **default version to use at runtime**, and click **Add** (3). <br/><img src="images/Prep147.png" width="800" /><br/>

18.	Click **x** to close the **retention_ml** service display. <br/><img src="images/Prep-11-18.png" width="800" /><br/>

19.	Click the **Variables** tab at the top of the diagram. <br/><img src="images/Prep-11-19.png" width="800" /><br/>

20. Select **customer (unavailable)** in the **Data** variables list. <br/><img src="images/Prep-11-20.png" width="800" /><br/>

21.	Click **Select…** in the **Details** pane. <br/><img src="images/Prep-11-21.png" width="800" /><br/>

22.	Select **decision_mlsamples_telco_retention_data_CustomerRecord** as the **Business Object**. <br/><img src="images/Prep-11-22.png" width="800" /><br/>

23.	Select **subscription (unavailable)** in the **Data** variables list. <br/><img src="images/Prep-11-23.png" width="800" /><br/>

24.	Click **Select…** in the **Details** pane. <br/><img src="images/Prep-11-24.png" width="800" /><br/>

25. Select **decision_mlsamples_telcor_etention_data_Subscription** as the **Business Object**. <br/><img src="images/Prep-11-25.png" width="800" /><br/>

26.	Select **retentionOffer (unavailable)** in the **Data** variables list. <br/><img src="images/Prep-11-26.png" width="800" /><br/>

27.	Click **Select…** in the **Details** pane. <br/><img src="images/Prep-11-27.png" width="800" /><br/>

28.	Select **decision_mlsamples_telco_retention_data_Offer** as the **Business Object**. <br/><img src="images/Prep-11-28.png" width="800" /><br/>

29.	Click the **Diagram** tab. <br/><img src="images/Prep-11-29.png" width="800" /><br/>

30.	Select **retentionOffer** on the **Operation** selector in the **Implementation** tab below the diagram.<br/><img src="images/Prep-11-30.png" width="800" /><br/>

31.	Click **Open** in the Input and Output mapping. <br/><img src="images/Prep-11-31.png" width="800" /><br/>

32.	Click **Insert suggestions**. <br/><img src="images/Prep-11-32.png" width="800" /><br/>

33.	Click the **Output mapping** tab. <br/><img src="images/Prep-11-33.png" width="800" /><br/>

34.	Click **Insert suggestions**. <br/><img src="images/Prep-11-34.png" width="800" /><br/>

35.	Click **OK**  <br/><img src="images/Prep-11-35.png" width="800" /><br/>

36. Click **Preview**  <br/><img src="images/Prep-11-36.png" width="800" /><br/> <inline-notification text="If the preview window displays an error, just logout and login again from your Cloud pak instance or wait a little bit and try again until the background operations are completed. "></inline-notification> 

37.	Enter **'Sarah Miller'** (1) in the **Search customer** field and click **Search** (2). <br/><img src="images/Prep165.png" width="800" /><br/>

38.	Click **Get offer**. <br/><img src="images/Prep166.png" width="800" /><br/>

39.	If you get a response without an error message, you are ready to demo.
<br/><img src="images/Prep167.png" width="800" /><br/>
**[Go to top](#top)**

</details>

## **PREPARE TO GIVE THE DEMO**
<span id="importFlow"></span>
<details markdown="1">

<summary>Open these resources before starting the demonstration</summary>

**1 - SkyTalk call center application**<br/>
1. Log in to Cloud Pak for Business Automation. Use the bookmark and credentials saved in step 2.<br/>
2. Expand the **top menu** (1), select the **arrow** icon (2) in the **Design** row, and click **Business applications** (3).<br/><img src="images/Prep168.png" width="800" /><br/>
3. Hover the mouse over the **SkyTalk call center Application** tile and click **Preview**.<br/><img src="images/Prep169.png" width="800" /><br/>
4. The **SkyTalk - Call Center** application opens.<br/><br/> <img src="images/Prep170.png" width="800" /><br/>

**2 - IBM Cloud Pak for Business Automation**<br/>
1. Click **IBM Cloud Pak / Automation**.<br/><img src="images/Prep171.png" width="800" /><br/>
2. The **Cloud Pak for Business Automation** home page opens.<br/><img src="images/Prep172.png" width="800" /><br/>

**3 - Watson Studio**<br/>
1. Go to the <a href="http://cloud.ibm.com" target="_blank" rel="noreferrer">IBM Cloud environment</a> and log in using your personal credentials. Ensure you are in your Cloud Pak for Data instance.<br/><br/>
2. Click the **Resource list** menu icon (1) and then select **Watson Studio-xx** (2).<br/><img src="images/Prep173.png" width="800" /><br/>
3. Click **Launch in IBM Cloud Pak for Data**.<br/><img src="images/Prep174.png" width="800" /><br/>
4. **Watson Studio** opens.<br/><img src="images/Prep175.png" width="800" /><br/>

**4 - SkyTalk customer retention policy.pdf**<br/>
1. Click this link to open <a href="./files/Retention Policy v2 RH.pdf" target="_blank" rel="noreferrer">SkyTalk customer retention policy.pdf.</a>
<br/>

**[Go to top](#top)**

</details>

## **AFTER EACH DEMO**
<span id="importFlow"></span>
<details markdown="1">

<summary>1 - Undeploy the two Watson Machine Learning services</summary>
1. Click the **SkyTalk production space** deployment.
<br/><img src="images/Prep176.png" width="800" /><br/>
2. Click the **Deployments** tab (1). Click the **three dots** icon in the **Lifetime value** row and select **Delete** (2). <br/><br/>Click **Delete** again to confirm the deletion. <br/> <inline-notification text="As soon as the two services are deleted, your Watson Machine Learning Lite subscription quota is not consumed anymore."></inline-notification><br/><img src="images/Prep177.png" width="800" /><br/>
3. Repeat step 2 and delete the deployment for the **churn prediction** row.
4. Click **Watson Studio** to return to the Watson Studio home page.
<br/><img src="images/Prep178.png" width="800" /><br/>
5. Click the **SkyTalk customer retention** project.
<br/><img src="images/Prep179.png" width="800" /><br/>
6. Click the **Assets** tab.
<br/><img src="images/Prep180.png" width="800" /><br/>
7. Click the **three dots** icon in the **Churn prediction 2** AutoAI experiment row.
<br/><img src="images/Prep181.png" width="800" /><br/>
8. Click **Delete**.
<br/><img src="images/Prep182.png" width="800" /><br/>
9. Click **Delete** again to confirm the removal.
<br/><img src="images/Prep183.png" width="800" /><br/>
<br/>

**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>2 - Reset the demo to its beginning state</summary>
1. Go to the previously opened **Cloud Pak for Automation** browser tab. Click **Customer retention**.
<br/><img src="images/Prep184.png" width="800" /><br/>
2. Click **Open**.
<br/><img src="images/Prep185.png" width="800" /><br/>
3. Select the **Initial retention** tile.
<br/><img src="images/Prep186.png" width="800" /><br/>
4. Click **Retention offer**.
<br/><img src="images/Prep187.png" width="800" /><br/>
5. Hover the mouse over the purple **Customer Churn** rounded box.
<br/><img src="images/Prep188.png" width="800" /><br/>
6. Click the **trash** icon to delete the node.
<br/><img src="images/Prep189.png" width="800" /><br/>
7. Click **Initial retention** in the breadcrumb menu.
<br/><img src="images/Prep190.png" width="800" /><br/>
8. Click the **three dots** icon that appears when you move your cursor over the **Customer Churn** predictive model row.
<br/><img src="images/Prep191.png" width="800" /><br/>
9. Click **Delete**.
<br/><img src="images/Prep192.png" width="800" /><br/>
10. Click **Delete** to confirm.
<br/><img src="images/Prep193.png" width="800" /><br/>
11. Only the **Retention offer** predictive model should remain.
<br/><img src="images/Prep194.png" width="800" /><br/>

**[Go to top](#top)**

</details>

## **PREPARATION REQUIRED TO GIVE THIS DEMO AGAIN**
<span id="importFlow"></span>
<details markdown="1">
<summary>1 - Redeploy both ML models in Watson Studio </summary>
Before starting a new demo, you must redeploy the two ML models you previously created.
<br/>
<inline-notification text="Anytime your ML services are deployed, your Machine Learning Lite subscription quota is consumed. To avoid running out of Watson ML quota, undeploy your ML services whenever you are not practicing or giving this demo. "></inline-notification>
<br/>
The **Reset the demo to its beginning state** step on this page below contains the process to undeploy the services and stop the billing process.
<br/>
Redeploy your ML services approximately 15 minutes prior to practicing or giving this demo.
<br/>
1. Go to <a href="http://cloud.ibm.com" target="_blank" rel="noreferrer">**IBM Cloud **</a>.<br/>
2. Enter your **IBM ID**. If you do not have one, create a new one.<br/>
3. Expand the **top menu** (1) and then select **Resource list** (2).<br/><img src="images/Prep195.png" width="800" /
<br/>
4. Click **Watson Studio-2D** in the **Services and software** section.<br/><img src="images/Prep196.png" width="800" /><br/>
5. Click **Launch in IBM Cloud Pak for Data**.<br/><img src="images/Prep197.png" width="800" /><br/>
6. From the Watson Studio environment, select the **SkyTalk production space** deployment.
<br/><img src="images/Prep198.png" width="800" /><br/>
7. Click the **Assets** tab.<br/><img src="images/Prep199.png" width="800" /><br/>
8. Deploy the **Skytalk churn prediction** by clicking the corresponding rocket icon that appears when you hover over the right side of the row.<br/><img src="images/Prep200.png" width="800" /><br/>
9. Select **Online** (1), name the deployment **churn** (2), and click **Create** (3).<br/><img src="images/Prep201.png" width="800" /><br/>
10. Deploy the **SkyTalk lifetime value prediction** by clicking the corresponding rocket icon that appears when you hover over the right side of the row.<br/><img src="images/Prep202.png" width="800" /><br/>
11. Select **Online** (1), name the deployment **'Lifetime value'** (2), and click **Create** (3).<br/><img src="images/Prep203.png" width="800" /><br/>
12. Click the **Deployments** tab. Ensure the two services are deployed.<br/><img src="images/Prep204.png" width="800" /><br/>

**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>2 - Reconnect both ML models to Automation Decision Services</summary>
1. Log in to Cloud Pak for Business Automation. Use the bookmark and credentials saved in step 2.<br/>
2. Click the recent automation **Customer retention**.<br/><img src="images/Prep205.png" width="800" /><br/><inline-notification text="You should have no deployed automation services, since they have been removed after the previous demo. Otherwise, remove them as explained in the <strong>After each demo</strong> section."></inline-notification><br/>
3. Click **Open**.<br/><img src="images/Prep206.png" width="800" /><br/>
4. Click **Retention ML**.<br/><img src="images/Prep207.png" width="800" /><br/>
5. Click the **Customer Churn** model on the **Models** tab.<br/><img src="images/Prep208.png" width="800" /><br/>
6. Click **Edit Configuration**.
<br/><img src="images/Prep209.png" width="800" /><br/>
7. Click **Next**.<br/><img src="images/Prep210.png" width="800" /><br/>
8. Expand the **SkyTalk churn prediction model** (1), select the **CHURN** deployment (2), and click **Next** (3).
<br/><img src="images/Prep211.png" width="800" /><br/>
9. Click **Next**.<br/><img src="images/Prep212.png" width="800" /><br/>
10.	Click **Run** to test the invocation.<br/><img src="images/Prep213.png" width="800" /><br/>
11.	If the test succeeds, click **Next**.<br/><img src="images/Prep214.png" width="800" /><br/>
12.	Click **Generate from test output**.<br/><img src="images/Prep215.png" width="800" /><br/>
13.	Click **OK**.<br/><img src="images/Prep216.png" width="800" /><br/>
14.	Click **Apply**.<br/><img src="images/Prep217.png" width="800" /><br/>
15.	Return to the **Retention ML** using the breadcrumb menu.<br/><img src="images/Prep218.png" width="800" /><br/>
16.	Click **Customer lifetime value** and then repeat previous steps 2 - 12, expanding and selecting the **Customer lifetime value ML** model.<br/><img src="images/Prep219.png" width="800" /><br/>
17.	Click the **Retention offer** model.<br/><img src="images/Prep220.png" width="800" /><br/>
18. Select the **Run** tab.<br/><img src="images/Prep51.png" width="800" /><br/>
19. Select the **High value profile** test file (1) and click **Run** (2).<br/><br/><inline-notification text="The <strong>retention offer</strong> should display. Click <strong>Run</strong> again if you get a timeout error the first time."></inline-notification><br/><img src="images/Prep221.png" width="800" /><br/>Your result should match the screen below:<br/><img src="images/Prep222.png" width="800" /><br/>

**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>3 - Redeploy the decision service</summary>
1. Click **Customer retention** in the breadcrumb menu.<br/><img src="images/Prep223.png" width="800" /><br/>
2. Select the **Share changes** tab.<br/><img src="images/Prep224.png" width="800" /><br/>
3. Click the **share all changes** box (1) and click **Share** (2).<br/><img src="images/Prep225.png" width="800" /><br/>
4. Click **Share** to push the updates to the Git repository.<br/><img src="images/Prep226.png" width="800" /><br/>
5. Select the **View history** tab.<br/><img src="images/Prep227.png" width="800" /><br/>
6. Click **Version +** in the row with the deployment you just created.<br/><img src="images/Prep228.png" width="800" /><br/>
7. Name the version number **'2.0.0'** (1). Click **Create** (2).<br/><img src="images/Prep229.png" width="800" /><br/>
8. Click the **Deploy** tab.<br/><img src="images/Prep230.png" width="800" /><br/>
9. Expand the latest version.<br/><img src="images/Prep231.png" width="800" /><br/>
10. Click **Deploy** in the **Retention ML** row.<br/><inline-notification text="Make sure you do not click the <strong>Initial retention</strong> decision service."></inline-notification><br/><img src="images/Prep232.png" width="800" /><br/>
11. Click **Deploy** when prompted.<br/><img src="images/Prep233.png" width="800" /><br/>
12. Wait for the deployment to finish (1). Click **Business Automations** (2) in the breadcrumb menu.<br/><img src="images/Prep234.png" width="800" /><br/>
13. The most recently deployed service displays. Click the **three dots** icon (1) and then select **Publish** (2).<br/><img src="images/Prep235.png" width="800" /><br/>
14. Click **Publish**.<br/><img src="images/Prep236.png" width="800" /><br/><inline-notification text="If the service fails to publish, wait for 5 minutes and try again."></inline-notification><br/>
15. Ensure the service appears as **Published**.<br/><img src="images/Prep237.png" width="800" /><br/>

**[Go to top](#top)**

</details>
<span id="importFlow"></span>
<details markdown="1">

<summary>4 - Reconnect the decision services to the call center application</summary>
This step must be performed anytime a new version of the **SkyTalk_rentention_DS** is deployed. Make sure only the latest deployed DS is published to prevent **Data renaming issues** when reimporting the new service
<br/>

Once your decision service is deployed, repeat the Application configuration strating from **step 11.12**
<br/>

**[Go to top](#top)**
</details>
***

Click [here](demo-script) to go to the **Demo script** on the next tab.