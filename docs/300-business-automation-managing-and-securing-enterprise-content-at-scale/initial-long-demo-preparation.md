---
title: Managing and securing enterprise content at scale
  400-level live demo
description: Managing and securing enterprise content at scale (ROKS) 400-level live demo
tabs: [ 'Demo preparation', 'Demo script']
---

export const Title = () => (
  <span>
    <h1 style="font-size:60px;"> Managing and securing enterprise content at scale<br/> 400-level live demo (ROKS)</h1>
  </span> );


![Managing and securing banner](./images/Content-management-400-Prep-GitHub-banner.jpg)

<span id="top"></span>

**WARNING AS OF JANUARY 27, 2023**: Due to an issue with OCP 4.10.x on Tech Zone, Cloud Pak for Business Automation reservations are randomly failing. If you are unable to find the icp4adeploy-cp4ba-access-info ConfigMap in the setup below (Step 1.11), you will know the deployment has failed. If that happens, please delete the failed environment and make a new reservation.

| DEMO OVERVIEW | |
| :---         | :--- |
| **Scenario overview** | This demo shows how IBM’s content management capabilities allow organizations to securely organize, manage and collaborate on documents and other types of content. To illustrate this, we’ll show how the capabilities are used to streamline a company’s hiring process. |
| **Demo products** | Cloud Pak for Business Automation |
| **Demo capabilities** | Content management |
| **Demo script** | A complete demo script is on the second tab above. <br/><br/> This demo script has multiple tasks, that each have multiple steps. In each step, you have the details about what you need to do (**Actions**), what you can say while delivering this demo step (**Narration**), and what diagrams and screenshots you will see. <br/><br/> This demo script is a suggestion, and you are welcome to customize based on your sales opportunity. Most importantly, practice this demo in advance. If the demo seems easy for you to execute, the customer will focus on the content. If it seems difficult for you to execute, the customer will focus on your delivery. |
| **Demo downloads** | • <a href="./ICNParallelDocumentApproval.pep" target="_blank" rel="noreferrer">ICNParallelDocumentApproval.pep</a> <br/> • <a href="./ICNSequentialDocumentApproval.pep" target="_blank" rel="noreferrer">ICNSequentialDocumentApproval.pep</a> <br/> • <a href="./P8TeamspaceTemplates.templates" target="_blank" rel="noreferrer">P8TeamspaceTemplates.templates</a> <br/> • <a href="./Resource files.zip" target="_blank" rel="noreferrer">Resource files.zip</a> |
| **Required versions** | Cloud Pak for Business Automation V22.0.1 |
| **How to get support** | **For IBMers:** <br/>• Contact <a href="https://ibm-cloud.slack.com/archives/C0124J683GW" target="_blank" rel="noreferrer">#itz-techzone-support</a> or <a href="mailto:techzone.help@ibm.com">techzone.help@ibm.com</a> regarding issues with reserving and provisioning Tech Zone environments.<br/>• Contact <a href="https://ibm-cloud.slack.com/archives/C0216F39ACU" target="_blank" rel="noreferrer">#platinumdemos-automation-support</a> regarding issues with setting up and running this demo. <br/><br/> **For Business Partners:** <br/>• Contact <a href="mailto:techzone.help@ibm.com">Tech Zone Support</a> regarding issues with reserving and provisioning Tech Zone environments.<br/>• Contact <a href="mailto:automationplatinumdemos@ibm.com"> Automation Platinum Demos Support</a> regarding issues with setting up and running this demo. |

<InlineNotification>There will be two Content Management demos in the Automation Platinum Demos collection - a simple version on SaaS and this deep dive version on ROKS. <br/><br/>The SaaS version is quick to install but only shows a single persona (which will be you, using your intranet credentials). This ROKS version is a more realistic scenario that shows three users collaborating. In this ROKS version, your customer will see how role-based redaction allows privileged users to see content that is hidden from other users. This demo also shows how multiple users can collaborate on and approve enterprise content.<br/><br/> The simpler SaaS version is not able to show these capabilities because the security requirements of the SaaS environment limit that demo to a single persona. The disadvantage of this ROKS version is that it takes longer to install. The ROKS version has several advantages, however, that include:<br/>
•	showing collaboration between multiple personas<br/>
•	showing role-based security<br/>
•	a great foundation you can extend into your own custom demo<br/>
•	a great start for building a customer POC<br/>
•	a great way for you to learn FileNet<br/><br/>*The SaaS version will be added to this collection by end of February 2023.</InlineNotification>

## **DEMO INSTALLATION AND SETUP**

<details>

<summary>1 - Provision a Cloud Pak for Business Automation environment</summary>

<br/>

Install Cloud Pak for Business Automation **22.0.1** or provision a pre-installed ROKS environment. To reserve your pre-installed ROKS instance, follow these steps:

<br/>

1. To reserve a preinstalled instance of Cloud Pak for Business Automation (CP4BA) V22.0.1 on Red Hat OpenShift, complete the form <a href="https://techzone.ibm.com/my/reservations/create/63059d83575f2b00183cfe6a" target="_blank" rel="noreferrer">here</a>. If you do not have a sales opportunity, select the purpose **Practice / Self-Education** to create a 3-day reservation (which can be extended to 8 days).

<br/>

2. You will receive a confirmation email confirming the instance is provisioning.

<br/>

3. You will receive a second email once the environment is provisioned. This email contains information, such as URLs, allowing you to connect to the instance.<br/>If you have issues connecting to your instance, please contact <a href="mailto:techzone.help@ibm.com">TechZone support</a> or refer to the installation documentation <a href="https://github.ibm.com/jgoodhue/cp4ba-roks-install" target="_blank" rel="noreferrer">here</a>.

<br/>

4. The full installation of the Cloud Pak for Business Automation will take an additional 6-8 hours after you receive the second email (containing the environment access instructions).

<br/>

Confirm the install is ready using the following instructions to validate the <strong>icp4adeploy-cp4ba-access-info</strong> ConfigMap has been created (this is final setup step for the CP4BA).

<br/>

5. Select the **Cluster URL** from the second email.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep1.png" width="800" /><br/>

6. Ensure you are on an **ITZ account**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep2.png" width="800" /><br/>

7. Ensure there are no **Alerts** for the cluster.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep3.png" width="800" /><br/>

8. Click **OpenShift web console**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep4.png" width="800" /><br/>

9. Expand **Workloads** (1) and click **Config Maps** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep5.png" width="800" /><br/>

10. Expand the **All Projects** menu (1) and select **cp4ba** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep6.png" width="800" />

<br/>

&nbsp<InlineNotification>If the ConfigMap does not appear after 8 hours, refer to the <a href="https://github.ibm.com/jgoodhue/cp4ba-roks-install" target="_blank" rel="noreferrer">ROKS help site</a> or contact <a href="mailto:techzone.help@ibm.com">Tech Zone Support</a>. </InlineNotification><br/> 

<br/>

11.	Type **'access'** (1) in the search field and click **icp4adeploy-cp4ba-access-info** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep7.png" width="800" /><br/>

12.	Scroll down to **ADS-designer-access-info** in the **Data** section.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep8.png" width="800" /><br/>When the ADS designer access info is present in the data file, this indicates that the installation is complete and you are ready to proceed.

<br/>

&nbsp<InlineNotification>Please contact  <a href="mailto:techzone.help@ibm.com">Tech Zone Support</a> if you don’t see the access file info after 8 hours.</InlineNotification>

<br/>

**[Go to top](#top)**

</details>

<details>

<summary>2 - Bookmark URLs and logins</summary>

<br/>

In this section you will collect the links to the required CP4BA capabilities and use them to make a cheat sheet to use through the demo.

<br/>

This demonstration uses two IBM content management products:

<br/>

1. **IBM FileNet Content Manager**: IBM FileNet Content Manager offers enterprise-level scalability and flexibility to access and manage all forms of content and automate records management to help meet compliance needs. At the core of the platform are repository services for capturing, managing, and storing your business-related digital assets. 

<br/>

2. **IBM Content Navigator**: IBM Content Navigator is a web client that provides users with a console for working with content from multiple content servers. IBM Content Navigator also enables users to create custom views of the content on the web client by creating teamspaces, which provide a focused view of the relevant documents, folders, and searches that a team needs to complete their tasks.<br/> 

&nbsp<InlineNotification>More info about IBM FileNet Content Manager and IBM Content navigator can be found <a href="https://www.ibm.com/docs/en/cloud-paks/cp-biz-automation/21.0.3?topic=software-filenet-content-manager" target="_blank" rel="noreferrer">here</a>.</InlineNotification><br/>

This is a sample of a completed cheat sheet (what you have at the end of Step 2):<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep341.png" width="800" /><br/>

For this demo, IBM Content Navigator, Content Platform Engine administration (ACCE), and Business Automation Studio use the same username (cp4admin) and password (unique to each CP4BA instance). However, they have unique URLs .<br/><br/>Let’s collect the URLs and passwords for the demo cheat sheet.<br/><br/>

1. Click **Workloads** to expand the menu.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep9.png" width="800" /><br/>

2. Select **ConfigMaps**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep10.png" width="800" /><br/>

3. Type **'access'** in the search field (the results will automatically filter).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep11.png" width="800" /><br/>

4. Click the **icpdeploy-cp4ba-access-info** ConfigMap.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep12.png" width="800" /><br/>

&nbsp<InlineNotification>Copy the <strong>password</strong> to your cheat sheet – this is the ‘cp4admin’ user's password for the demo.</InlineNotification>

<br/>

5. Scroll to **navigator-access-info**. Bookmark the **Business Automation Navigator for CP4BA** URL and copy to your cheat sheet. This URL opens IBM Content Navigator during the demo and demo prep.<br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep13.png" width="800" /><br/>

5. Scroll to **cpe-access-info** in the data section.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep14.png" width="800" /><br/>

6. Bookmark the **Content Platform Engine administration** (ACCE) URL and copy to your cheat sheet.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep15.png" width="800" /><br/>

7. Scroll to **bastudio-access-info**. Bookmark the **Cloudpak Dashboard** URL. This URL opens Business Automation Studio during the demo and demo prep.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep16.png" width="800" /><br/> 

**[Go to top](#top)**

</details>

<details>

<summary>3 - Create users </summary>

<br/>

The demo uses three personas: Henry (the HR Manager), Debby (the hiring Manager), and Patrick (the payroll Manager). Let’s configure the individual accounts for Henry, Debby, and Patrick in the CP4BA Instance. 

<br/>

Start by creating their logins.

<br/>

1. Select **Secrets**. <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep18.png" width="800" /><br/>

2. Type '**openldap**' (1) in the search field and click **cp4adeploy-openldap-customldif** (2). <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep19.png" width="800" /><br/>

3. Click **Actions** (1) and then select **Edit Secret** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep20.png" width="800" />

<br/>

Let’s update the '**ldapfile_user.ldif file**.' 

<br/>

4. To see all the information, update the file in a separate text editor (e.g., Microsoft Word). <br/><br/>Copy the existing text in the **Value** field to your text editor.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep21.png" width="800" /><br/>

5. Copy the user data below for Henry, Debby, and Patrick. Find the user name '**rrServiceUser**' (1) and paste their user data after it (2).
<br/>
dn: uid=henry,dc=example,dc=org<br/>
uid: henry	<br/>
cn: henry<br/>
sn: henry<br/>
userpassword: henry2022<br/>
objectClass: top<br/>
objectClass: posixAccount<br/>
objectClass: organizationalPerson<br/>
objectClass: inetOrgPerson<br/>
objectClass: person<br/>
uidNumber: #####+1<br/>
gidNumber: XXXXXX<br/>
homeDirectory: /home/henry/<br/>
mail: henry@example.org<br/><br/>
dn: uid=debby,dc=example,dc=org<br/>
uid: debby<br/>
cn: debby<br/>
sn: debby<br/>
userpassword: debby2022<br/>
objectClass: top<br/>
objectClass: posixAccount<br/>
objectClass: organizationalPerson<br/>
objectClass: inetOrgPerson<br/>
objectClass: person<br/>
uidNumber: #####+2<br/>
gidNumber: XXXXXX<br/>
homeDirectory: /home/debby/<br/>
mail: debby@example.org<br/><br/>
dn: uid=patrick,dc=example,dc=org<br/>
uid: patrick<br/>
cn: patrick<br/>
sn: patrick<br/>
userpassword: patrick2022<br/>
objectClass: top<br/>
objectClass: posixAccount<br/>
objectClass: organizationalPerson<br/>
objectClass: inetOrgPerson<br/>
objectClass: person<br/>
uidNumber: #####+3<br/>
gidNumber: XXXXXX<br/>
homeDirectory: /home/patrick/<br/>
mail: patrick@example.org <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep22.png" width="800" /><br/>

<br/>

6. Copy the **gidNumber** (1) and the **uidNumber** (2) from the **rrServiceUser**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep23.png" width="800" /><br/>

7. Replace **XXXXXX** in the **gidNumber field** in **henry**'s user data with the gidNumber from the rrServiceuser. Repeat for debby and patrick. <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep24.png" width="800" /><br/>	 

8. Assign a new **uidNmber** for henry, debby, and patrick by starting with the **uidNumber** for **rrServiceUser** and adding 1 to each sequentially. <br/><br/>For example, if rrServiceUser uidNumber: 14583116, then **henry**’s uidNumber is 14583117, **debby**’s uidNumber is 14583118, and **patrick**’s uidNumber is 14583119.<br/><br/>The final new users should look like the below:<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep25.png" width="800" /><br/>

9. Copy and paste the following text at the end of the **GeneralUsers** list:<br/><br/>
member: uid=henry,dc=example,dc=org<br/>
member: uid=debby,dc=example,dc=org<br/>
member: uid=patrick,dc=example,dc=org<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep26.png" width="800" /><br/>

10.	Copy and paste the following text at the end of the **TaskUsers** list:<br/><br/>
member: uid=henry,dc=example,dc=org<br/>
member: uid=debby,dc=example,dc=org<br/>
member: uid=patrick,dc=example,dc=org<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep27.png" width="800" /><br/>

11.	Copy all the text from your text editor and replace the text in the **Value** field (1). Click **Save** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep28.png" width="800" /><br/>

12.	Click **Reveal values**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep29.png" width="800" /><br/>

13.	Verify that your updates were saved. <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep30.png" width="800" /><br/>

14. Now restart the LDAP pod to implement the updates. Start by clicking **Pods**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep31.png" width="800" /><br/>

15.	Type '**openldap**' in the search field. <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep32.png" width="800" /><br/>

16.	When the results display, click the **menu** icon (1) in the row containing '**icp4adeploy-openldap-deploy-XXXXX-XXX**' (the numbers at the end will vary). Select **Delete Pod** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep33.png" width="800" /><br/>

17.	Click **Delete**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep34.png" width="800" /><br/>

18.	A new pod will automatically re-create. <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep35.png" width="800" />

<br/>

In a real implementation, Focus Corp’s Cloud Pak administrator would configure the access rights for henry, debby and patrick. Let’s find the Cloud Pak administrator password, log into Content Platform Engine administration (ACCE), and make the access changes necessary for the demo. 

<br/>

19.	Click **Secrets**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep36.png" width="800" /><br/>

20.	Type '**auth-idp**' in the search field (1) and click **platform-auth-idp-credentials** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep38.png" width="800" /><br/>

21.	Click **Reveal values**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep39.png" width="800" /><br/>

22.	Copy the **admin_password** and **admin_username** to your cheat sheet.<br/><br/><InlineNotification>These logins are not the same as the 'cp4admin' credentials copied for CP4BA capabilities earlier in Step 2.</InlineNotification><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep40.png" width="800" />

<br/>

Let’s add henry, debby, and patrick to the CP4A user administration panel.

<br/>

23.	Open Business Automation Studio using the URL from your cheat sheet.<br/><br/> 

24.	Select **EnterpriseLDAP** in the **Log in with** drop down menu.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep357.png" width="800" /><br/>

25.	Enter the **Username: ‘admin’** and the **Password** (1) from step 3.22. Click **Log in** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep41.png" width="800" /><br/>

26.	Click **Manage users**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep44.png" width="800" /><br/>

27.	Click **Add users +**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep45.png" width="800" /><br/>

28.	Type '**henry**' in the search field (1) and click **henry** in the results list (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep46.png" width="800" /><br/>

29.	Add '**debby**' and '**patrick**' by repeating the previous step.<br/><br/>

30.	Verify that **henry**, **debby** and **patrick** are added (1). Click **Next** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep47.png" width="800" /><br/>

31.	Select **Assign roles directly** (1). Click **Next** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep48.png" width="800" /><br/>

32.	Select the boxes next to **Automation Administrator** and **Automation Developer** (1). Click **Next** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep49.png" width="800" /><br/>

33.	Click **Add**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep50.png" width="800" /><br/>

34.	Verify that **henry**, **debby**, and **patrick** are added.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep51.png" width="800" /><br/>

35.	**Log out** from Business Automation Studio.

<br/>

Let's add **henry** as an Administrator in IBM Content Navigator so he can show role-based redactions during the demo.

<br/>

36.	Open IBM Content Navigator using the URL from your cheat sheet. Select **Enterprise LDAP** in the **Log in with** drop down menu (1). Enter **Username ‘cp4admin’** and the **Password** (2) from your cheat sheet. Click **Log in** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep52.png" width="800" /><br/>

37.	Click the **hamburger menu** icon at the top left of the page.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep53.png" width="800" /><br/>

38.	Click **Administration**. <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep54.png" width="800" /><br/>

39.	Click **Settings**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep55.png" width="800" /><br/>

40.	Click the **Administrators** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep56.png" width="800" /><br/>

41.	Type '**henry**' (1) in the **New Administrator** field. Click **Add** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep57.png" width="800" /><br/>

42.	Click **Save and Close**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep58.png" width="800" /><br/>

43.	Hover your mouse over the **user** icon (1) and click **Log Out** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep59.png" width="800" /><br/>

44.	Open IBM Content Navigator using the URL from your cheat sheet. Select **Enterprise LDAP** in the **Log in with** drop down menu (1). Enter the **Username: henry** and **Password**: henry2022 (1). Click **Log in** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep60.png" width="800" /><br/>

45.	Click the **hamburger menu** icon at the top left of the page.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep61.png" width="800" /><br/>

46.	Make sure the **Administration** settings menu displays as an option for **henry** to select.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep62.png" width="800" /><br/>If **Administration** does not appear, go back to step 3.25 and repeat the steps.

<br/>

**[Go to top](#top)**

</details>

<details>

<summary>4 - Configure the built-in content review workflows </summary>

<br/>

In this section, you will configure your demo to use the integrated parallel and sequential document review workflows.

<br/>

1.	Open the Content Platform Engine administration (ACCE) using the URL from your cheat sheet. Enter **Username ‘cp4admin’** and the **Password** (1) from your cheat sheet. Click **Log in** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep63.png" width="800" /><br/>
 
2. Expand **Object Stores** (1) to configure the object store and double click **CONTENT** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep64.png" width="800" /><br/>

3. Click **Administrative** to expand the menu.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep65.png" width="800" /><br/>

4. Click **Workflow System** (1) and then click **Isolated Regions** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep66.png" width="800" /><br/>

5. Select **content_region_name**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep67.png" width="800" /><br/>

6. Click **Web Applications**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep68.png" width="800" /><br/>

7. Click **IBM Content Navigator**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep69.png" width="800" /><br/>

8. Paste the IBM Content Navigator URL from your cheat sheet into the **Server base URL** field (1) and click **OK** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep70.png" width="800" /><br/>

9. Click **Save**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep71.png" width="800" /><br/>

10.	Expand **content_region_name**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep72.png" width="800" /><br/>

11.	Expand **User Queues**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep73.png" width="800" /><br/>

12.	Click **Inbox**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep74.png" width="800" /><br/>

13.	Click **System Fields**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep75.png" width="800" /><br/>

14.	Click **Add**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep76.png" width="800" /><br/>

15.	In the **Add System Fields** list select:<br/>
•	**F_StartTime**<br/>
•	**F_Comment**<br/>
•	**F_Response**<br/>
•	**F_StepName**<br/>
•	**F_Deadline**<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep77.png" width="800" /><br/>

16.	Click **OK**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep78.png" width="800" /><br/>

17.	Click **Save** (1) and wait for the save to be done. Click **In-baskets** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep79.png" width="800" /><br/>

18.	Click **New**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep80.png" width="800" /><br/>

19.	Type ‘**FC review inbox**’ (1) and then click the **Columns and Labels** tab (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep81.png" width="800" /><br/>

20.	Click **Add**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep82.png" width="800" /><br/>

21.	Select the **Show system fields** box.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep83.png" width="800" /><br/>

22.	In the list, select the boxes next to:<br/>
•	**F_Comment**<br/>
•	**F_CreateTime**<br/>
•	**F_overdue**<br/>
•	**F_Response**<br/>
•	**F_StartTime**<br/>
•	**F_StepName**<br/>
•	**F_Deadline**<br/>
•	**F_Subject**<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep84.png" width="800" /><br/>

23.	Click **OK**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep85.png" width="800" /><br/>
 
24.	Change the **Column Labels** to:<br/>
•	**F_CreateTime (Time) -> Creation time**<br/>
•	**F_Subject (String) -> Subject**<br/>
•	**F_Overdue (Integer) -> Overdue**<br/>
•	**F_StartTime (Time) -> Start time**<br/>
•	**F_Comment (String) -> Comment**<br/>
•	**F_Response (String) -> Response**<br/>
•	**F_Deadline (Time) -> Due date**<br/>
•	**F_StepName -> Workflow step name**<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep86.png" width="800" /><br/>

25.	Click **OK**. <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep87.png" width="800" /><br/>

26.	Click **Save**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep88.png" width="800" /><br/>

27.	Click **Security**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep89.png" width="800" /><br/>

28.	Click **Add**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep90.png" width="800" /><br/>

29.	Type ‘**henry**’ in the search field (1) and click **Search** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep91.png" width="800" /><br/>

30.	Click the row with user **henry** (1). Select **Query** (2) and **Process** (3). Click the **right-facing arrow** (4). <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep92.png" width="800" /><br/>

31.	Click **OK**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep93.png" width="800" /><br/>

32.	Click **Add**. Add **debby** and **patrick** by repeating the previous three steps.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep94.png" width="800" /><br/>

33.	Once the three users are added, click **Save**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep95.png" width="800" /><br/>

34.	Expand **Application Spaces**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep96.png" width="800" /><br/>

35.	Click **DefaultApplication**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep97.png" width="800" /><br/>

36.	Click the **Security** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep98.png" width="800" /><br/>

37.	Click **Add**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep99.png" width="800" /><br/>

38.	Type ‘**henry**’ in the search field (1) and click **Search** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep100.png" width="800" /><br/>

39.	Click the row with user **henry** (1) and then click the **right-facing arrow** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep101.png" width="800" /><br/>

40.	Add **debby** and **patrick** by repeating the previous two steps.

<br/>

41.	Once the three users are added, click **OK**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep102.png" width="800" /><br/>

42.	Click **Save** (1) and then click the **Roles** tab (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep103.png" width="800" /><br/>

43.	Click **New**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep104.png" width="800" /><br/>

44. Type ‘**FC Approvers**’ in the **Name** field (1) and click the **In-Baskets and Members** tab (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep105.png" width="800" /><br/>

45.	Click **Add** in the **In-Baskets** section.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep106.png" width="800" /><br/>

46.	Select **FC review inbox** (1) and click **OK** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep107.png" width="800" /><br/>

47.	Click **Add** in the **Members** section.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep108.png" width="800" /><br/>

48.	Type ‘**henry**’ in the search field (1) and click **Search** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep109.png" width="800" /><br/>

49.	Click the row with user **henry** (1) and then click the **right-facing arrow** (2). <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep110.png" width="800" /><br/>

50.	Add **debby** and **patrick** by repeating the previous two steps.

<br/>

51.	Click **OK**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep112.png" width="800" /><br/>

52.	Click **OK**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep113.png" width="800" /><br/>

53.	Click **Save**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep114.png" width="800" /><br/>

54.	Open IBM Content Navigator and sign in using the URL from your cheat sheet, the username ‘cp4admin’, and the password from your cheat sheet.<br/><br/>Click the **hamburger menu** icon (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep115.png" width="800" /><br/>

55.	Click **Administration**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep116.png" width="800" /><br/>

56.	Click **Connections**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep117.png" width="800" /><br/>

57.	Click the **Repositories** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep118.png" width="800" /><br/>

58.	Double-click **content**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep119.png" width="800" /><br/>

59.	Click **Connect . . . **<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep120.png" width="800" /><br/>

60.	Enter **Username ‘cp4admin’** (1) and the **Password** (2) from your cheat sheet. Click **Log In** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep121.png" width="800" /><br/>

61.	Click the **Configuration Parameters** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep122.png" width="800" /><br/>

62.	Make sure **pe_conn_content:1** is selected in the **Workflow connection point**: field(1). Select the **Yes** bubble for both the **Display workflow definition class:** (2) and **Display form template class:** (3). <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep123.png" width="800" /><br/>

63.	Scroll down and click the **Allow users to merge and split pages that have role-based redactions** box.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep124.png" width="800" /><br/>

64.	Click **Save and Close**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep125.png" width="800" /><br/>

65.	Refresh your browser window. 
 
<br/>

**[Go to top](#top)**

</details>

<details>

<summary>5 - Create your demonstration desktop</summary>

<br/>

In this section, you will configure IBM Content Navigator to host your demonstration.

<br/>

1. Open IBM Content Navigator using the URL from your cheat sheet. Log in using the ‘cp4admin’ username and password from your cheat sheet.<br/><br/><InlineNotification>Make sure to use the <strong>enterprise LDPA</strong> authentication method. If you see a page saying no teams were found, close the browser menu and open IBM Content Navigator again.</InlineNotification><br/>

2. Click the **hamburger menu** icon.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep127.png" width="800" /><br/>

3. Click **Administration**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep128.png" width="800" /><br/>

4. Select **Viewer Maps**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep129.png" width="800" /><br/>

5. Select the **Default viewer map** (1) and click **Copy** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep130.png" width="800" /><br/>

6. Type ‘**FCViewerMap**’ in the **Name** field.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep131.png" width="800" /><br/>

7. In the Viewer table, select the **FileNet Content Manager – Video Viewer** row (1) and move it to the top of the table using the **Move Up** button (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep132.png" width="800" /><br/>

8. In the Viewer table, select the **FileNet Content Manager – Daeja ViewONE Virtual** row (1) and make it the second row of the table using the **Move Up** button (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep133.png" width="800" /><br/>

9. Click **Save and Close**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep134.png" width="800" /><br/>

10.	Click the **Desktops** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep135.png" width="800" /><br/>

11.	Select the **contentdesktop** row (1) and click **Copy** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep136.png" width="800" /><br/>

12.	Type ‘**FocusCorp**’ in the **Name** field.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep137.png" width="800" /><br/>

13.	On the **General** tab, in the **Desktop Configuration** section, select **FCViewerMap** as your **Default Viewer Map**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep138.png" width="800" /><br/>
 
14.	Scroll down to the **Additional settings** (1) section and select the **Set as the default desktop** (2) and **Enable this desktop for FileNet P8 workflow email notification** (3) boxes.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep139.png" width="800" /><br/>

15.	Scroll down and click the **downward arrow** (1) to expand the **Plug-ins** section (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep140.png" width="800" /><br/>

16.	Click the **Select the deployed plug-ins to enable for use with the desktop** bubble.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep141.png" width="800" /><br/>

17.	Uncheck the boxes next to all plug-ins except the **External Application Service plug-in**, **Application Discovery plug-in**, and **Platform Plug-in**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep142.png" width="500" /><br/>

18.	Click **Save**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep143.png" width="800" /><br/>

19.	Click the **x** to close the information box and refresh your browser.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep144.png" width="800" /><br/>

Let’s add the parallel and sequential workflow definitions.

<br/>

20.	Click the **Browse Content** tile.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep145.png" width="800" /><br/>

21.	Click **New Folder**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep146.png" width="800" /><br/>

22.	Type ‘**Workflows**’ (1) in the **Folder Name**. Click **Add** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep147.png" width="800" /><br/>

23.	Click **Workflows**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep148.png" width="800" /><br/>

24.	Download the <a href="./ICNParallelDocumentApproval.pep" target="_blank" rel="noreferrer"><strong>ICNParallelDocumentApproval.pep</strong></a> file and drag it to the **Workflows** folder.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep149.png" width="800" /><br/>

25.	For **Properties Class**, expand the **Document** menu, select **Workflow Definition** (1) and click **OK** (2). Click **Add** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep150.png" width="800" /><br/>

26.	Repeat the last two steps to add the **ICNSequentialDocumentApproval.pep** file to the **Workflows** folder.

<br/>

27.	Right-click **ICNParrallelDocumentApproval.pep** (1), select **Workflow** (2) and click **Transfer Workflow** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep151.png" width="800" /><br/>

28.	Click **Transfer**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep152.png" width="800" /><br/>

29.	Repeat the last two steps to transfer the <a href="./ICNSequentialDocumentApproval.pep" target="_blank" rel="noreferrer">ICNSequentialDocumentApproval.pep</a> file. 
 
<br/>

**[Go to top](#top)**

</details>

<details>

<summary>6 - Configure role-based redactions</summary>

<br/>

1. Open IBM Content Navigator using the URL from your cheat sheet. Log in using username ‘cp4admin’ and password from your cheat sheet.

<br/>

2. Click the **hamburger menu** icon (2) and select **Administration** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep153.png" width="800" /><br/>

3. Double-click **Role-based Redactions**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep154.png" width="800" /><br/>

4. Click **New Redaction Reason**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep155.png" width="800" /><br/>

5. Type ‘**Private Information**’ (1) in the redaction reason **Name** field and ‘**Candidate personal information**’ (2) in the **Description** field.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep156.png" width="800" /><br/>

6. Click **Save**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep157.png" width="800" /><br/>

7. Click the **Policies and Roles** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep158.png" width="800" /><br/>

8. If prompted, sign into the object store using the **Username ‘cp4admin’** and **Password** (1) from your cheat sheet. Click **Log in** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep159.png" width="800" /><br/>

9. Click **New Redaction Role**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep160.png" width="800" /><br/>

10. Type ‘**FC redaction viewer**’ (1) in the redaction **Name** field, select **Viewer** as the **Type** (2), and type ‘**Redaction viewer role at FocusCorp**’ (3) in the **Description** field.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep161.png" width="800" /><br/>

11. Select **Users** as the redaction role **Membership**. Enter ‘**Patrick**’ in the search field and click the **magnifier** icon (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep162.png" width="800" /><br/>

12.	Move **patrick** to the **Selected users and groups** list by selecting **patrick** (1) in the **Available Users** list, ensuring that the **Default access** is set to **Allow** (2), and clicking the **right-facing arrow** (3). <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep163.png" width="800" /><br/>

13.	Repeat the two previous steps to add **cp4admin** to the **Selected Users and Groups** list. <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep164.png" width="800" /><br/>

14.	Click the **Policies and Roles** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep165.png" width="800" /><br/>

15.	Click **New Redaction Role**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep166.png" width="800" /><br/>

16.	Type ‘**FC redaction editor**’ (1) in the redaction **Name** field, select **Editor** as the **Type** (2), and type ‘**Redaction editor role at FocusCorp**’ in the **Description** (3) field.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep167.png" width="800" /><br/>

17.	Move **cp4admin** to the **Selected Redaction Editors** list by selecting **cp4admin** (1) in the **Available Redaction Editors** list, ensuring that the **Default access** is set to **Allow** (2), and clicking the **right-facing arrow** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep168.png" width="800" /><br/>

18.	Click **New Editors . . .**<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep169.png" width="800" /><br/>

19. Click the **Search for** menu field and select **Users**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep170.png" width="800" /><br/>

20.	Type ‘**henry**’ in the search criteria field (1) and click the **magnifier** icon (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep171.png" width="800" /><br/>

21.	Select **henry** (1) in the **Available** list and click the **right-facing arrow** (2) to move **henry** to the **Selected** list.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep172.png" width="800" /><br/>

22.	Click **Add**. <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep173.png" width="800" /><br/>

23.	Verify that **henry** and **cp4admin** are added to the **Selected Redaction Editors** list (1). If they are, click **Save and Close** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep174.png" width="800" /><br/>

24.	Click the **Policies and Roles** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep175.png" width="800" /><br/>

25.	Click **New Redaction Policy**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep176.png" width="800" /><br/>

26.	Type ‘**FC Redaction policy**’ (1) in the policy **Name** field and then type ‘**Focus Corp redaction policy**’ in the **Description** field (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep177.png" width="800" /><br/>

27.	Move **Private Information** to the **Selected Reasons** list by selecting **Private Information** (1) and clicking the **right-facing arrow** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep178.png" width="800" /><br/>

28.	Move **FC redaction editor** to the **Selected Editor Roles** list by selecting **FC redaction editor** (1) and clicking the **right-facing arrow** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep179.png" width="800" /><br/>

29.	Move **FC redaction viewer** to the **Selected Viewer Roles** list by selecting **FC redaction viewer** (1) and clicking the **right-facing arrow** (2). <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep180.png" width="800" /><br/>

30.	Click **Save and Close**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep181.png" width="800" /><br/>

31.	If prompted, sign into the object store using the **Username ‘cp4admin’** and **Password** (1) from your cheat sheet. Click **Log in** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep182.png" width="500" /><br/>

32.	Click the **Reasons** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep183.png" width="800" /><br/>

33.	Check that your **Private Information** redaction reason is linked to the **content** object store.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep184.png" width="800" /><br/>

34.	Click the **x **to close the **Role-based Redactions** menu.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep185.png" width="800" /><br/>

<br/>

**[Go to top](#top)**

</details>

<details>

<summary>7 - Create your document data model</summary>

<br/>

In this section, we will configure the demonstration’s document metadata. To create this document metadata, we will create choice lists (steps 7.1 – 7.16), create property templates that use the choice lists (steps 7.17 – 7.36), and then use the property templates to create a new document type called ‘Application Document’ (steps 7.37 – 7.49).

First, create three choice lists.

<br/>

1. Open the Content Platform Engine administration (ACCE) using the URL from your cheat sheet. Log in using the username ‘cp4admin’ and password from your cheat sheet.

<br/>

2. Click **CONTENT**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep186.png" width="800" /><br/>

3. Expand **Data Design**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep187.png" width="800" /><br/>

4. Click **Choice Lists**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep188.png" width="800" /><br/>

5. Click **New**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep189.png" width="800" /><br/>

6. Type ‘**Department names**’ (1) in the **Display name** field and click **Next** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep190.png" width="800" /><br/>

7. Select **String** (1) and then click **Next** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep191.png" width="800" /><br/>

8. Click **New Items**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep192.png" width="800" /><br/>

9. Type ‘**R&D**’ (1) in the **Display name** field. Update the **Value** by clicking anywhere in the white space of the **New Items** box (2). Click **Add** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep193.png" width="800" /><br/>

10.	Repeat the previous step to add these department **Name**s and **Value**s:<br/>
•	**HR/HR**<br/>
•	**Accounting/Accounting**<br/>
•	**Sales/Sales**<br/>
•	**Marketing/Marketing**<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep194.png" width="500" /><br/>

11.	Click **OK**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep195.png" width="500" /><br/>

12.	Click **Next**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep196.png" width="800" /><br/>

13.	Click **Finish**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep197.png" width="800" /><br/>

14.	Click **Close**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep198.png" width="800" />

<br/>

Now create two more choice lists, one for ‘Document types’ and one for ‘Document sources’.

<br/>

15.	To create the ‘Document types’ choice list, repeat steps 7.4 – 7.14.<br/><br/><InlineNotification> When repeating step 7.6, type <strong>‘Document types’</strong> in the <strong>Display name</strong> field.</InlineNotification>

 <br/> 
Add these document types:<br/>
•	  <strong>Resume</strong><br/>
•	  <strong>ID</strong><br/>
•	  <strong>Diploma</strong><br/>
•	  <strong>Motivation letter</strong><br/>
•	  <strong>Evaluation form</strong><br/>
•	  <strong>Candidate video</strong><br/>
•	  <strong>HR process</strong><br/>
•	  <strong>Other</strong><br/>
<br/>Before repeating steps 7.11 – 7.14, your list should match:<br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep205.png" width="800" /><br/>

16. To create the ‘Document sources’ choice list, repeat steps 7.4 – 7.14.

<br/><InlineNotification> When repeating step 7.6, type <strong>‘Document sources’</strong> in the <strong>Display name</strong> field.</InlineNotification>

<br/>

Add these document sources:<br/>
•	  <strong>Internal</strong><br/>
•	  <strong>External</strong><br/>
<br/>Before repeating steps 7.11 – 7.14, your list should match:<br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep216.png" width="800" />

<br/>

Let's create the property templates.

<br/>

17.	Click **Property Templates**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep221.png" width="800" /><br/>

18.	Click **New**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep222.png" width="800" /><br/>

19.	Type ‘**Candidate Name**’ in the **Display name** field.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep223.png" width="800" /><br/>

20.	Click **Next**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep224.png" width="800" /><br/>

21.	Select **String** as **Data Type** (1) and click **Next** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep225.png" width="800" /><br/>

22.	Click **Next**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep226.png" width="800" /><br/>

23.	Click **Next**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep227.png" width="800" /><br/>

24.	Click **Finish**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep228.png" width="800" /><br/>

25.	Click **Close**. <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep229.png" width="800" /><br/>

26.	Repeat steps 7.17 – 7.25 to create an ‘Application Date’ property template.

<br/>

<InlineNotification>When repeating step 7.21, select <strong>’Date Time’</strong> as the Data Type.</InlineNotification>

<br/>

Now let’s use the new choice lists to create the Department Name, Document Type and Document Source property templates.

<br/>

27.	Click **New**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep230.png" width="800" /><br/>

28.	Type '**Department Name**’ (1) in the **Display name** field and click **Next** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep231.png" width="800" /><br/>

29.	Select **String** as the **Data type** (1) and click **Next** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep232.png" width="800" /><br/>

30.	Check the **Assign choice list** box.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep233.png" width="800" /><br/>

31.	Select **Department names**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep234.png" width="800" /><br/>

32.	Click **Next**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep235.png" width="800" /><br/>

33.	Click **Next**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep236.png" width="800" /><br/>

34.	Click **Finish**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep237.png" width="800" /><br/>

35.	Click **Close**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep238.png" width="800" /><br/>

36.	Repeat steps 7.27 – 7.35 to create the other two property templates:<br/>
•	**Document Type** (when repeating step 7.31, select the **Document types** choice list)<br/>
•	**Document Source** (when repeating step 7.31, select the **Document sources** choice list)<br/><br/> Finally, let’s create a new document type called ‘Application Document.’ This will help classify documents in Filenet Content Manager.  

<br/>

37.	Click **Classes**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep239.png" width="800" /><br/>

38.	Click **Document**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep240.png" width="800" /><br/>

39.	Click **Actions** (1) and select **New Class** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep241.png" width="800" /><br/>

40.	Type ‘**Application Document**’ (1) in the **Display name** field and click **Next** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep242.png" width="800" /><br/>

41.	Click **Next**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep243.png" width="800" /><br/>

42.	Click **Finish**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep244.png" width="800" /><br/>

43.	Click **Open**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep245.png" width="800" /><br/>

44.	Click the **Property Definitions** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep246.png" width="800" /><br/>

45.	Click **Add**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep247.png" width="800" /><br/>

46.	Type ‘**Candidate**’ (1) and click **Filter** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep248.png" width="500" /><br/>

47.	Select **Candidate Name** (1) and click **OK** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep249.png" width="500" /><br/>

48.	Repeat steps 7.45 – 7.47 to add these four document properties:<br/>
•	**Application Date **<br/>
•	**Department Name **<br/>
•	**Document Type **<br/>
•	**Document Source**<br/>

<br/>

<InlineNotification><strong>Application Date</strong> has a different <strong>Data Type</strong> from the others: <strong>Date Time</strong>.</InlineNotification> 


49.	Click **Save** (1) and **Close** (2).<br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep250.png" width="800" /><br/>


**[Go to top](#top)**

</details>

<details>

<summary>8 - Prepare your document files</summary>

<br/>

During the demonstration, documents will be added to the content management platform. These are:

<br/>

•	**HR Documents**: A set of forms that the organization uses to hire new candidates.<br/>
•	**Candidate files**: Files related to a given applicant (John Doe in our demo). These files are documents sent by the applicant or pre-filled forms that reduce the demonstration duration.

<br/>

You can find these documents in this <a href="https://ibm.box.com/s/vnhbpo81sd2d1qtyt9crbm5mp05aii92" target="_blank" rel="noreferrer">Resource files.zip</a> archive.

<br/>

1. Get the zip file from the GitHub link.

<br/>

2. Unzip the **Resource files.zip** archive in your local disk in the repository of your choice.

<br/>

3. Open the folder containing the HR and John doe’s repositories so that it is available during the entire demo.

<br/>

**[Go to top](#top)**

</details>

<details>

<summary>9 - Create your default repository</summary>

<br/>

Let’s create repository to store the documents we will need to configure the demonstration.

<br/>

1. Open IBM Content Navigator using the URL from your cheat sheet. Log in using the username ‘cp4admin’ and password from your cheat sheet.

2. Click **Browse Content** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep251.png" width="800" /><br/>

3. Click **New Folder**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep252.png" width="800" /><br/>

4. Type ‘**ECM Platinum Demo**’ in the **Folder Name** field (1) and click **Add** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep253.png" width="800" /><br/>

5. Click the **ECM Platinum Demo** folder.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep254.png" width="800" /><br/>

6. Drag the **HR Documents** files from your local files to the **ECM Platinum Demo** folder.<br/><br/><InlineNotification>The HR Documents are in the <a href="./Resource files.zip" target="_blank" rel="noreferrer">Resource files.zip</a>.</InlineNotification><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep255.png" width="800" /><br/>

7. Click **Add**.<br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep256.png" width="800" /><br/>
 
8. Click the **x** to close the **Browse Content** view.<br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep257.png" width="800" /><br/>


**[Go to top](#top)**

</details>

<details>

<summary>10 - Create your document entry template</summary>

<br/>

Let’s create a document entry template that will ask for metadata any time a new document is added to the Teamspace during the demo.

<br/>

1. Click **Entry Template Manager**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep258.png" width="800" /><br/>
 
2. Click **New Entry Template** (1) and select **Document Entry Template** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep259.png" width="800" /><br/>

3. Type ‘**HR Application Document Entry Template**’ in the **Name field**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep260.png" width="800" /><br/>

4. In the **Set the Item Storage Location** section, expand the **Default Save in location** drop down menu.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep353.png" width="800" /><br/>

5. Select the **content** Teamspace (1) and then select the **ECM Platinum Demo** (2) repository. Click **OK** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep261.png" width="800" /><br/>

6. In the **Set the Item Properties** section, expand the **Class** dropdown menu (1), select **Application Document** (2) and click **OK** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep262.png" width="800" /><br/>

7. Click **Edit Layout . . .**<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep263.png" width="800" /><br/>

8. Drag **Multiple Column Layout** to the design pane at the very top position. Make sure the blue line that indicates the position of the move matches this display:<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep264.png" width="800" /><br/>

Continue creating the entry template layout by moving the property fields to the appropriate place. The header is the **Candidate name** property. Document metadata property fields go in the left column and job role properties goes in the right column.

<br/> 

9. Start by dragging the **Document title** field to the top left template box.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep350.png" width="800" /><br/>

10.	Drag the **Department name** field to the top right template box.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep351.png" width="800" /><br/>

11.	Drag the **Candidate name** field to the top of the template box (above the column fields where the blue line will appear as shown in the following screenshot).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep352.png" width="800" /><br/>

12.	Move the remaining property fields in the table columns until the template matches:<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep266.png" width="800" /><br/>

13. Click the **Candidate Name** field (1) and click the box to set its value to **Required** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep267.png" width="800" /><br/>

14.	Click the **Document Source** field (1) and click the box to set its value to **Required** (2). Uncheck the box next to **Include empty choice** (3). Set the **Default Value** to **Internal** (4).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep268.png" width="800" /><br/>

15.	Repeat the previous step for both the **Department Type** and **Document Type** fields. All the settings should match the ones configured for Document Source.<br/><br/>The final design pane should match this:<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep269.png" width="800" /><br/>

16.	Click **Save and Close**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep270.png" width="800" /><br/>

17.	Click the **Hide the class** box.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep355.png" width="800" /><br/>

18.	Scroll down to the **Set the Item Security** section and click **Select . . .**<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep271.png" width="800" /><br/>

19.	Type ‘**henry**’ in the search for **Users** field.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep356.png" width="800" /><br/> 

20.	Select **henry** (1) in the **Available** list and click the **right-facing arrow** (2) to move the user to the **Selected** list.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep272.png" width="800" /><br/>

21.	Repeat the previous step to add **debby** and **patrick**.

<br/>

22.	Click the **Permissions** (1) drop down menu and select **Owner** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep273.png" width="800" /><br/>

23.	Click **Add**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep274.png" width="800" /><br/>

24.	Once **henry**, **debby**, and **patrick** are added (1), click the bubble next to **Hide the Security section** (2). Click **Save and Close** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep275.png" width="800" /><br/>

25.	Right-click **HR Application Document Entry Template** (1) and click **Properties** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep276.png" width="800" /><br/>

26.	Click the **Security** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep277.png" width="800" /><br/>

27.	Click **Select . . .** <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep278.png" width="800" /><br/>

28.	Search for ‘**henry**’ and click the right-facing arrow to add him to the **Selected** list. Repeat this process to add **debby** and **patrick** to the list. <br/><br/>Click the **Permissions** (1) drop down menu and select **Reader** (2). Click **Apply** (3) and then click **Close** (4).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep279.png" width="800" /><br/>

29.	Click **Save**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep280.png" width="800" /><br/>

30.	Click the **x** to close the **Entry Template Manager** view.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep282.png" width="800" /><br/>

**[Go to top](#top)**

</details>

<details>

<summary>11 - Create the Teamspace template</summary>

<br/>

The final preparation task is to create a Teamspace Template that the hiring team will use to collaborate with new applicants. Download the <a href="./P8TeamspaceTemplates.templates" target="_blank" rel="noreferrer"><strong>P8TeamspaceTemplates.templates</strong></a> file. 

<br/>

1. Open IBM Content Navigator using the URL from your cheat sheet. Log in using the username ‘cp4admin’ and password from your cheat sheet.

<br/>

2. Click the **Teamspaces** tile. <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep283.png" width="800" /><br/>

3. Click the **Templates** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep284.png" width="800" /><br/>
 
4. Click **Import**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep285.png" width="800" /><br/>
 
5. Click **Choose file**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep286.png" width="800" /><br/>
 
6. Select the **P8TeamspaceTemplates.templates** file (1) and click **Open** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep287.png" width="800" /><br/>

7. Click **Import**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep288.png" width="800" /><br/>

8. Double-click **FC Hiring Teamspace Template**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep289.png" width="800" /><br/>

9. Click the **Select Classes or Entry Templates** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep290.png" width="800" /><br/>

10.	Select **HR Application Document Entry Template** (1) and click **Add** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep291.png" width="800" /><br/>

11.	Click the **Folders and Documents Tree** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep292.png" width="800" /><br/>

12.	Click **HR Documents**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep293.png" width="800" /><br/>

13.	Click **Add Document**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep294.png" width="800" /><br/> 

14.	Click the **Search in** (1) drop down menu and select the **ECM Platinum Demo** (2). and click **OK** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep295.png" width="800" /><br/>

15.	Scroll to the **Search Criteria** section. In the **Property options** box, select **Is not Empty** (1) in the search criteria drop down menu (1) next to **Document Title**. Click **Search** (2). <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep296.png" width="800" /><br/>

16.	Select all the files (1) and click **OK** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep297.png" width="800" /><br/>

17.	Right-click **FC Evaluation form.docx** (1) and click **Properties** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep298.png" width="800" /><br/>

18.	Click the **Security** tab.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep299.png" width="800" /><br/>

19.	Click **Select... **<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep300.png" width="800" /><br/>
 
20.	Search for ‘**debby**’.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep301.png" width="800" /><br/>

21.	Select **debby** (1) and click the **right-facing arrow** (2) to add her to the **Selected** list.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep302.png" width="800" /><br/>

22.	Verify the **Permissions** role is **Owner** (1) and click **Add** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep303.png" width="800" /><br/>

23.	Click **Save**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep304.png" width="800" /><br/>

24.	Click **Validate**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep305.png" width="800" /><br/>

25.	Select the **FC Hiring Teamspace Template** (1), click the **Actions** (2) drop down menu, and click **Properties** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep306.png" width="800" /><br/>
 
26.	Click **Security**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep307.png" width="800" /><br/>

27.	Click **Select...**<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep308.png" width="800" /><br/>

28.	Type ‘**henry**’ (1) and click the **magnifier** icon (2). <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep309.png" width="800" /><br/>

29.	Select **henry** (1) and click the **right-facing arrow** (2) to add him to the **Selected** list.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep310.png" width="800" /><br/>
 
30.	Repeat the previous step to add **debby** and **patrick**.

<br/>

31.	Select **Reader** in the **Permissions** drop box (1) and click **Add** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep311.png" width="800" /><br/>

32.	Click **Save**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep312.png" width="800" /><br/>
 
33. Select the **FC Hiring Teamspace Template** (1), click the **Actions** (2) drop down menu, and click **Set as Default** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep313.png" width="800" /><br/>
 
34.	Click the **x** to close the Teamspaces view.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep314.png" width="800" /><br/>
 
**[Go to top](#top)**

</details>

<details>

<summary>12 - Create a finalized teamspace</summary>

<br/>

1. Open IBM Content Navigator using the URL from your cheat sheet. Enter the **Username ‘henry’** and the **Password ‘henry2022’** (1). Click **Log in** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep315.png" width="800" /><br/>
 
2. Click the **Teamspaces** tile.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep316.png" width="800" /><br/>
 
3. Click **New Teamspace**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep317.png" width="800" /><br/>
 
4. Type ‘**John Doe**’ (1) in the **Teamspace name** field and click **Select Users** (2). <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep318.png" width="800" /><br/>

5. Click **Add Users and Groups . . .** <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep319.png" width="800" /><br/>
 
6. Type ‘**debby**’ (1) and click the **magnifier** icon (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep320.png" width="800" /><br/>
 
7. Select **debby** (1) and click the **right-facing arrow** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep321.png" width="800" /><br/>
 
8. Repeat the previous step to add **patrick**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep322.png" width="800" /><br/>
 
9. Select **Member** (1) in the **Roles** menu and click **Add** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep323.png" width="800" /><br/>

10.	Click **Finish**. <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep324.png" width="800" /><br/>

11.	Click the **Candidate files** folder.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep325.png" width="800" /><br/>

12.	Open your local files containing John Doe’s application files.<br/><br/><InlineNotification>John Doe’s application files are in the <a href="./Resource files.zip" target="_blank" rel="noreferrer">Resource files.zip</a>.</InlineNotification><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep326.png" width="800" /><br/>
 
13.	Drag the **John Doe Diploma.pdf** file to the **Candidate files** folder.<br/>&nbsp<img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep327.png" width="800" /><br/>
 
14.	Type ‘**John Doe**’ for **Candidate Name** (1), set the **Document Type** to **Diploma** (2), set the **Document Source** to **External** (3), and set the **Department Name** to **R&D** (4). Click the **calendar** icon (5) and pick a day approximately three days in the future. Click **Add** (6).<br/>&nbsp<img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep328.png" width="800" /><br/>
 
15.	Repeat the previous two steps to add the other documents (individually) to the **Candidate Files** folder. Add the properties below to each document as you add them to the repository: <br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep329.png" width="800" /><br/>

16.	Click **John Doe Video.mp4**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep330.png" width="800" /><br/>

17.	Click **Bookmarks**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep331.png" width="800" /><br/>

18.	Click **New Bookmark**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep332.png" width="800" /><br/>

19.	Type ‘**Overview**’ (1) in the **Name** field. Type ‘**Tell me about yourself?**’ (2) in the description field. Click **OK** (3).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep333.png" width="800" /><br/>

20.	Click the **play** icon and wait until the question slide that indicates the next question. Click the **pause** icon (which is in the same place as the play icon).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep334.png" width="800" /><br/>

21.	Repeat steps 17 - 19 to add more bookmarks, one at each new question slide. Repeat this process until these bookmarks are added:

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

22.	The finalized bookmarks for the video should match the following:<br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep336.png" width="800" /><br/>
 
23.	Close the IBM Navigator Viewer window.

<br/>

**[Go to top](#top)**

</details>

## **PREPARE TO GIVE THIS DEMO**

<details>

<summary>1 - Before each demo</summary>

<br/>

Open these resources before starting the demonstration:
<br/>

1. The cheat sheet you created during demo preparation.

<br/>

2. Use the URL from your cheat sheet to open IBM Content Navigator in a browser tab.

<br/>

3.	Use the URL from your cheat sheet to open Content Platform Engine administration (ACCE) in a browser tab.

<br/>

4.	Use the URL from your cheat sheet to open Business Automation Studio in a browser tab.

<br/>

<InlineNotification>Do not log in now, you will do this during the demonstration.</InlineNotification>

</details>

<details>

<summary>2- Giving the demo again</summary>

<br/>

To give this demo again, you must do the following steps to reset the demo to its original state:

<br/>

1.	Delete the John Doe Teamspace.<br/>
2.	Delete the John Doe Demo Teamspace.<br/>
3.	Repeat Step 12 of this document.<br/>

<br/>

Follow these detailed instructions to delete the Teamspaces:

<br/>

1. Open IBM Content Navigator using the URL from your cheat sheet. Enter the **Username ‘henry’** and the **Password ‘henry2022’** (1). Click **Log in** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep337.png" width="800" /><br/>

2. Click the **Teamspaces** tile.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep338.png" width="800" /><br/>
 
3. Right-click the **John Doe** Teamspace (1) and click **Delete** (2).<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep339.png" width="800" /><br/>

4. Click **Delete**.<br/><br/><img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/400-business-automation-managing-and-securing-enterprise-content-at-scale-ROKS/images/Prep340.png" width="800" /><br/>

5. Repeat steps 3 and 4 to delete the **John Doe Demo** Teamspace.

<br/>

6. Repeat chapter 12 - Create a finalized Teamspace.

<br/>

**[Go to top](#top)**

</details>