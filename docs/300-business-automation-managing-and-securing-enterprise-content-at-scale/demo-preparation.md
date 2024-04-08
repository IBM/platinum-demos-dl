---
title: Managing and securing enterprise content at scale <br/>Technical Sales Level 3 demo
layout: preparation
banner: images/Prep-banner.png
---


<span id="top"></span>

| DEMO OVERVIEW | |
| :---         | :--- |
| **Scenario overview** | This demo shows how IBM’s content management capabilities allow organizations to securely organize, manage and collaborate on documents and other types of content. To illustrate this, we’ll show how the capabilities are used to streamline a company’s hiring process. |
| **Demo products** | Cloud Pak for Business Automation |
| **Demo capabilities** | Content management |
| **Demo intro slides** | Download the Introduction and Overview slides <a href="./files/Managing and Securing Enterprise Content at Scale Platinum Demo - Intro deck.pptx" target="_blank" rel="noreferrer">here</a>. This is a short deck of customer-facing slides that sets the context for the demo. |
| **Demo script** | A complete demo script is on the second tab above. You can download a printer-ready PDF of the demo script <a href="./files/Managing and Securing Enterprise Content at Scale Platinum Demo - PDF script.pdf" target="_blank" rel="noreferrer">here</a>. <br/> This demo script has multiple tasks, that each have multiple steps. In each step, you have the details about what you need to do (**Actions**), what you can say while delivering this demo step (**Narration**), and what diagrams and screenshots you will see. <br/> This demo script is a suggestion, and you are welcome to customize based on your sales opportunity. Most importantly, practice this demo in advance. If the demo seems easy for you to execute, the customer will focus on the content. If it seems difficult for you to execute, the customer will focus on your delivery. |
| **Demo downloads** | • <a href="./files/Demo-Installer-23-0-2.zip" target="_blank" rel="noreferrer">Demo installer archive</a><br/> • <a href="./files/Resource files.zip" target="_blank" rel="noreferrer">Resource files.zip</a><br/> • <a href="./files/P8TeamspaceTemplates.templates" target="_blank" rel="noreferrer">P8TeamspaceTemplates</a> <br/> |
| **Sales enablement video** | View the enablement video <a href="https://ibm.box.com/s/3y8p1y32ap5tpln6nb6iakncs44ip0xc" target="_blank" rel="noreferrer">here</a>. This video is for enablement purposes only (IBMers and Business Partners) and is not customer-ready. |
| **Required versions** | Cloud Pak for Business Automation V23.0.2 <br/> |
| **How to get support** | • Open a support case at <a href="https://techzone.ibm.com/help" target="_blank" rel="noreferrer">IBM Technology Zone Help</a> regarding issues with reserving and provisioning Tech Zone environments.<br/>• IBMers, contact <a href="https://ibm.enterprise.slack.com/archives/C06HT5PHLN9" target="_blank" rel="noreferrer">#ba-techlcd-support</a>  regarding issues with setting up and running this demo. |

## **DEMO INSTALLATION AND SETUP**

<span id="importFlow"></span>
<details markdown="1">

<summary>1 - Provision Cloud Pak for Business Automation environment</summary><br/>

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

<summary>2 - Validate your environment</summary><br/>
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

<summary>3 - Bookmark URLs and logins</summary><br/>

This demo shows how IBM Content Navigator manages content. A web-based console provides end-users the capability to securely access and work content assets, individually or with a team.

In this section, you will collect the links to access the required capabilities and use them to make a cheat sheet to use throughout the demo.

This is a sample completed cheat sheet:<br/><img src="./images/Prep-cheatsheet.png" width="500" /><br/>

Let’s collect the URLs and passwords for the demo cheat sheet.<br/>

1. Log in your Openshift console using the credentials provided in section 1 above.<br/>

2. Expand your user menu (1) and click **Copy login command** (2).<br/><img src="./images/Prep358.png" width="800" /><br/>

3. Click **Display Token**.<br/><img src="./images/Prep359.png" width="800" /><br/>

4. Copy the Admin **token** (1) and the Admin URL (2) to your cheat sheet.<br/><img src="./images/Prep360.png" width="800" /><br/>

5. Close the tab in your browser to return to the ROKS admin page.<br/>Let's get the URL, username, and password to access IBM Content Navigator.<br/>

6. Click  **ConfigMaps**.<br/><img src="./images/Prep10.png" width="800" /><br/>

7. Expand the **Project** menu (1) and select **cp4ba-starter** (2).<br/><img src="./images/Prep-cp4ba-starter.png" width="800" /><br/>

8. Type **‘access’** in the search field (the results will automatically filter).<br/><img src="./images/Prep-type-access.png" width="800" /><br/>

9. Click the **icpdeploy-cp4ba-access-info** ConfigMap.<br/><img src="./images/Prep-click-icpdeploy.png" width="800" /><br/>

10. Scroll to the **navigator-access-info** (1) section. Copy the **Business Automation Navigator for CP4BA** URL (2) to your cheat sheet as the IBM Content Navigator URL. Copy **username: cp4admin** and the **password** (3) to your cheat sheet as well. <br/><inline-notification text="This is the cp4admin user’s password for IBM Content Navigator and Business Automation Studio."></inline-notification><br/><img src="./images/Prep-cheat-sheet-info.png" width="800" /><br/>

**[Go to top](#top)**

</details>

<span id="importFlow"></span>
<details markdown="1">

<summary>4 - Execute setup script </summary><br/>

A script will configure IBM FileNet Content Manager (FNCM), IBM Cloud Pak for Business Automation (CP4BA) and parts of the IBM Content Navigator for the demo. Steps 4-7 explain the remaining manual configurations.<br/>

This automated configuration script uses the FNCM and CP4BA public APIs to:<br/>
1. Create the three personas used in this scenario: Henry (the HR Manager), Debby (the hiring Manager), and Patrick (the payroll Manager).
2. Create the document data model in FNCM.
3. Configure the built-in workflows used to validate documents.
4. Create and dedicated desktop in IBM Content Navigator.
5. Configure role-based redactions.
6. Create a document entry template.

<br/><inline-notification text="The following instruction are documented for an Apple Mac OS environment. For MS Windows users, proceed with the same commands using a Microsoft shell and executing the .BAT files."></inline-notification><br/>

1. Ensure you have Java 8 or later installed on your computer. Find your Java version by opening a Terminal window, typing the command "**java -version**" (1), and hitting enter. The **version** displays (2).<br/><img src="./images/Prep361.png" width="800" /><br/>If you do not have Java, download it from these locations:<br/>• IBMers with MacOS, use the <a href="https://w3.ibm.com/mac/" target="_blank" rel="noreferrer">Mac@IBM store</a>.<br/> • IBMers with PCs, use the <a href="https://w3.ibm.com/download/standardsoftware/PC/lang_en/issiCatalogPC.html" target="_blank" rel="noreferrer">PC@IBM store</a>.<br/> • Business Partners, use the <a href="https://www.oracle.com/java/technologies/downloads/" target="_blank" rel="noreferrer">Java downloads site</a> (or as directed by your internal IT department).<br/>

2. Download and unzip the <a href="./files/Demo-Installer-23-0-2.zip" target="_blank" rel="noreferrer">demo installer archive</a><br/> on a local folder of your computer.<br/>

3. Use a Terminal Shell window to navigate to the folder where the archive was unzipped:<br/><img src="./images/Prep362.png" width="800" /><br/>

4. Type **'cd ContentPlatinumDemoDeployment'** and hit enter to access the folder folder.<br/><img src="./images/Prep363.png" width="800" /><br/>

5. From your file browser, edit the **‘configurePlatinumDemoStarter.sh’** (.sh on Mac and .bat on Windows) file using the text editor of your choice.<br/><img src="./images/File-Browser.png" width="800" /><br/>

6. Replace the '<**ocpAdminURL**>' tag with the Admin URL from your cheat sheet (see step 2.3).<br/><img src="./images/Prep-4-6.png" width="800" /><br/>

7. Replace the '<**ocpAdminToken**>' tag with the Admin token from your cheat sheet (see step 2.3).<br/><img src="./images/Prep-4-7.png" width="800" /><br/>

8. Save and close the file (ctrl + s).

<br/>

9. On Mac: Make the file executable by typing **‘chmod 755 configureContentPlatinumDemoStarter.sh’** in the terminal window.<br/><img src="./images/Prep368.png" width="800" /><br/>

10. Type **‘./configureContentPlatinumDemoStarter.sh’** and hit enter to execute the script.<br/><img src="./images/Prep-4-10.png" width="800" /><br/>

11.	Wait for the execution to complete (1-3 minutes). <br/>After the execution completes, your display should match:<br/><img src="./images/Prep-4-11.png" width="800" /><br/>

<inline-notification text=" Review the entire display to check that all actions are <strong>Successful</strong> (meaning none <strong>Failed</strong> or were <strong>Skipped</strong>). The user login credentials should also display at the end of the script execution."></inline-notification><br/>

**[Go to top](#top)**

</details>

<span id="importFlow"></span>
<details markdown="1">

<summary>5 - Prepare your document files</summary><br/>

During the demo, documents related to the applicant John Doe will be added to the content management platform. These documents, called **Candidate files**, are documents sent by the applicant or pre-filled forms that reduce the demonstration duration.<br/>

1. Download the <a href="./files/Resource files.zip" target="_blank" rel="noreferrer">Resource files.zip</a> archive containing the documents.<br/>
2. Unzip the archive.<br/>
3. Open the folder containing the John Doe document repository.<br/>

**[Go to top](#top)**

</details>

<span id="importFlow"></span>
<details markdown="1">

<summary>6 - Create the Teamspace template</summary><br/>

Let's create a Teamspace template for the hiring team to use when collaborating on new applicants. Download the <a href="./files/P8TeamspaceTemplates.templates" target="_blank" rel="noreferrer"><strong>P8TeamspaceTemplates</strong></a> file.

1. Open IBM Content Navigator using the URL from your cheat sheet. Select **Enterprise LDAP** in the **Log in with** drop down menu (1). Enter **‘cp4admin’** as the **Username** and the **Password** (2) from your cheat sheet. Click **Log in** (3).<br/><img src="./images/Prep52.png" width="800" /><br/>

2. Click the **Teamspaces** tile. <br/><img src="./images/Prep283.png" width="800" /><br/>

3. Click the **Templates** tab.<br/><img src="./images/Prep284.png" width="800" /><br/>

4. Click **Import**.<br/><img src="./images/Prep285.png" width="800" /><br/>

5. Click **Browse** or **Choose file** (based on your browser).<br/><img src="./images/Prep344.png" width="800" /><br/><img src="./images/Prep286.png" width="800" /><br/>

6. Select the **P8TeamspaceTemplates** file (1) and click **Open** (2).<br/><img src="./images/Prep287.png" width="800" /><br/>

7. Click **Import**.<br/><img src="./images/Prep288.png" width="800" /><br/>

8. Double-click **FC Hiring Teamspace Template**.<br/><img src="./images/Prep289.png" width="800" /><br/>

9. Click the **Select Classes or Entry Templates** tab.<br/><img src="./images/Prep290.png" width="800" /><br/>

10.	Select **HR Application Document Entry Template** (1) and click **Add** (2).<br/><img src="./images/Prep291.png" width="800" /><br/>

11.	Click the **Folders and Documents Tree** tab.<br/><img src="./images/Prep292.png" width="800" /><br/>

12.	Click **HR Documents**.<br/><img src="./images/Prep293.png" width="800" /><br/>

13.	Click **Add Document**.<br/><img src="./images/Prep294.png" width="800" /><br/>

14.	Expand the **Search in** (1) drop down menu, select the **ECM Platinum Demo** (2) and click **OK** (3).<br/><img src="./images/Prep295.png" width="800" /><br/>

15.	Scroll to the **Search Criteria** section. In the **Property options** box, select **Is Not Empty** (1) in the search criteria drop down menu next to **Document Title**. Click **Search** (2). <br/><img src="./images/Prep296.png" width="800" /><br/>

16.	Select all the files (1) and click **OK** (2).<br/><img src="./images/Prep297.png" width="800" /><br/>

17.	Right-click **FC Evaluation form.docx** (1) and click **Properties** (2).<br/><img src="./images/Prep298.png" width="800" /><br/>

18.	Click the **Security** tab.<br/><img src="./images/Prep299.png" width="800" /><br/>

19.	Click **Select...**<br/><img src="./images/Prep300.png" width="800" /><br/>

20.	Search for **‘debby’**.<br/><img src="./images/Prep-6-20.png" width="800" /><br/>

21.	Select **debby** (1) and click the **right-facing arrow** (2) to add her to the **Selected** list.<br/><img src="./images/Prep-6-21.png" width="800" /><br/>

22.	Verify the **Permissions** role is **Owner** (1) and click **Add** (2).<br/><img src="./images/Prep-6-22.png" width="800" /><br/>

23.	Click **Save**.<br/><img src="./images/Prep304.png" width="800" /><br/>

24.	Click **Validate**.<br/><img src="./images/Prep305.png" width="800" /><br/>

25.	Select the **FC Hiring Teamspace Template** (1), click the **Actions** (2) drop down menu, and click **Properties** (3).<br/><img src="./images/Prep306.png" width="800" /><br/>

26.	Click **Security**.<br/><img src="./images/Prep307.png" width="800" /><br/>

27.	Click **Select...**<br/><img src="./images/Prep308.png" width="800" /><br/>

28.	Type ‘**henry**’ (1) and click the **magnifier** icon (2). <br/><img src="./images/Prep-6-28.png" width="800" /><br/>

29.	Select **henry** (1) and click the **right-facing arrow** (2) to add him to the **Selected** list.<br/><img src="./images/Prep-6-29.png" width="800" /><br/>

30.	Repeat the previous step to add **debby** and **patrick**.<br/>

31.	Select **Reader** in the **Permissions** drop box (1) and click **Add** (2).<br/><img src="./images/Prep-6-31.png" width="800" /><br/>

32.	Click **Save**.<br/><img src="./images/Prep312.png" width="800" /><br/>

33. Select the **FC Hiring Teamspace Template** (1), click the **Actions** (2) drop down menu, and click **Set as Default** (3).<br/><img src="./images/Prep313.png" width="800" /><br/>

34.	Click the **x** to close the Teamspaces view.<br/><img src="./images/Prep314.png" width="800" /><br/>

35. Log out of IBM Content Navigator.<br/>

**[Go to top](#top)**

</details>

<span id="importFlow"></span>
<details markdown="1">

<summary>7 - Create a finalized teamspace</summary><br/>

1. Open IBM Content Navigator using the URL from your cheat sheet. Select **Enterprise LDAP** in the **Log in with** drop down menu (1). Enter the **Username: 'henry'** and **Password: 'henry'** (2). Click **Log in** (3).<br/><img src="./images/Prep60.png" width="800" /><br/>

2. Click the **Teamspaces** tile.<br/><img src="./images/Prep316.png" width="800" /><br/>

3. Click **New Teamspace**.<br/><img src="./images/Prep317.png" width="800" /><br/>

4. Type ‘**John Doe**’ (1) in the **Teamspace name** field and click **Select Users** (2). <br/><img src="./images/Prep318.png" width="800" /><br/>

5. Click **Add Users and Groups...** <br/><img src="./images/Prep319.png" width="800" /><br/>

6. Type ‘**debby**’ (1) and click the **magnifier** icon (2).<br/><img src="./images/Prep-7-6.png" width="800" /><br/>

7. Select **debby** (1) and click the **right-facing arrow** (2).<br/><img src="./images/Prep-7-7.png" width="800" /><br/>

8. Repeat the previous step to add **patrick**.<br/><img src="./images/Prep-7-8.png" width="800" /><br/>

9. Select **Member** (1) in the **Roles** menu and click **Add** (2).<br/><img src="./images/Prep-7-9.png" width="800" /><br/>

10.	Click **Finish**. <br/><img src="./images/Prep324.png" width="800" /><br/>

11.	Click the **Candidate files** folder.<br/><img src="./images/Prep325.png" width="800" /><br/>

12.	Open your local files containing John Doe’s application files.<br/><inline-notification text="John Doe’s application files are in the <a href='./files/Resource files.zip' target='_blank' rel='noreferrer'>Resource files.zip</a> archive."></inline-notification><br/><img src="./images/Prep326.png" width="800" /><br/>

13.	Drag the **John Doe Diploma.pdf** file to the **Candidate files** folder.<br/><img src="./images/Prep327.png" width="800" /><br/>

14.	Type ‘**John Doe**’ for **Candidate Name** (1), set the **Document Type** to **Diploma** (2), set the **Document Source** to **External** (3), and set the **Department Name** to **R&D** (4). Click the **calendar** icon (5) and pick a day approximately three days in the future. Click **Add** (6).<br/><img src="./images/Prep328.png" width="800" /><br/>

15.	Repeat the previous two steps to add the John Doe's **Resume**, **Video**, and **Drivers License** documents (individually) to the **Candidate Files** folder. Add the properties below to each document as you add them to the repository: <br/><img src="./images/Prep329.png" width="800" /><br/>

16.	Click **John Doe Video.mp4**.<br/><img src="./images/Prep330.png" width="800" /><br/>

17.	Click **Bookmarks**.<br/><img src="./images/Prep331.png" width="800" /><br/>

18.	Click **New Bookmark**.<br/><img src="./images/Prep332.png" width="800" /><br/>

19.	Type ‘**Overview**’ (1) in the **Name** field. Type ‘**Tell me about yourself?**’ (2) in the description field. Click **OK** (3).<br/><img src="./images/Prep333.png" width="800" /><br/>

20.	Click the play icon and then pause the video at the next question slide.<br/><img src="./images/Prep334.png" width="800" /><br/>

21.	Repeat actions 17 - 19 to add more bookmarks, one at each new question slide. Repeat this process until these bookmarks are added:

<br/>

| Bookmark name | Time | Description |
| --- | --- | --- |
| Overview | 00:00:00 | Tell me about yourself? |
| Hiring reasons | 00:00:25 | Why should we hire you? |
| Last job | 00:00:34 | Why did you leave your last job? |
| Weaknesses | 00:00:46 | What is your greatest weakness? |
| Strengths | 00:00:53 | What are your greatest strengths? |
| Other interests | 00:01:03 | What do you like to do outside of work? |

<br/>

22.	The finalized bookmarks for the video should match the following:<br/><img src="./images/Prep336.png" width="800" /><br/>

23.	Log out and close the IBM Navigator Viewer window.

<br/>

**[Go to top](#top)**

</details>

## **PREPARE TO GIVE THIS DEMO**

<span id="importFlow"></span>
<details markdown="1">

<summary>1 - Before each demo</summary><br/>

Have these resources ready before starting the demonstration:
<br/>

1. Open the cheat sheet you created during demo preparation.
<br/>
2. Open the folder containing John Doe's candidate files (unzipped during step 5 - Prepare your document files).
<br/>
3. Use the URL from your cheat sheet to open IBM Content Navigator in a browser tab.

<br/>

<inline-notification text="Do not log in now, you will do this during the demonstration."></inline-notification>

</details>

<span id="importFlow"></span>
<details markdown="1">

<summary>2- Giving the demo again</summary><br/>

To give this demo again, you must do the following steps to reset the demo to its original state:<br/>

1.	Delete the John Doe Teamspace.
<br/>
2.	Delete the John Doe Demo Teamspace.
<br/>
3.	Repeat **Demo preparation** step **7 – Create a finalized teamspace**.

<br/>

Follow these detailed instructions to delete the Teamspaces:

<br/>

1. Open IBM Content Navigator using the URL from your cheat sheet. Enter the **Username** ‘henry’ and the **Password** ‘henry’ (1). Click **Log in** (2).<br/><img src="./images/Prep-username-password-henry.png" width="800" /><br/>

2. Click the **Teamspaces** tile.<br/><img src="./images/Prep338.png" width="800" /><br/>

3. Right-click the **John Doe** Teamspace (1) and click **Delete** (2).<br/><img src="./images/Prep339.png" width="800" /><br/>

4. Click **Delete**.<br/><img src="./images/Prep340.png" width="800" /><br/>

5. Repeat actions 3 and 4 in this step to delete the **John Doe Demo Teamspace**.<br/>

6. Repeat **Demo preparation** step **7 – Create a finalized teamspace**.

<br/>

**[Go to top](#top)**

</details>

***

Click [here](demo-script) to go to the **Demo script** on the next tab.