---
title: Managing and securing enterprise content at scale <br/>Technical Sales Level 3 demo
layout: demoscript
banner: images/Script-banner.png
---

<span id="top"></span>

<span id="spanID"></span>
<details markdown="1">

<summary>Introduction</summary><br/>

Today we’ll see how IBM’s content management capabilities are used to manage and secure content across an organization at scale. We’ll see how using an enterprise platform to share and manage content enhances productivity, increases security and mitigates risk.

Using an HR hiring scenario, we’ll show how to easily configure a centralized repository for document collaboration. We’ll look at how to secure documents using redaction and role-based access capabilities. And we’ll see how the built-in workflow capabilities are used to manage document approvals.

We’re using a hiring example, but the same document repository can extend and scale to many scenarios across your enterprise.

Let’s get started!

(Printer-ready PDF of demo script <a href="./files/Managing and Securing Enterprise Content at Scale Platinum Demo - PDF script.pdf" target="_blank" rel="noreferrer">here</a>)

<br/>

</details>

<span id="spanID"></span>
<details markdown="1">

<summary>1 - Configuring a new space for document collaboration</summary>

<br/>

| **1.1** | **Create a new teamspace** |
| :--- | :--- |
| **Narration** | Focus Corp’s HR department needed a way to organize job candidate documents and facilitate collaboration among hiring decision-makers. When a candidate submits a new application, the HR manager uses the company's enterprise content management system to create a teamspace, which is a dedicated place to share information and collaborate. |
| **Action** &nbsp; 1.1.1 | Show the IBM Content Navigator screen that you opened during demo preparation. Sign in using the **Username: henry** and **Password: henry**. Click **Log in**. <br/> |
| **Action** &nbsp; 1.1.2 | Click the **Teamspaces** tile. <br/><img src="./images/Script2.png" width="800"  /><br/> |
| **Action** &nbsp; 1.1.3 | Click **New Teamspace**. <br/><img src="./images/Script3.png" width="800" /> |
| **Action** &nbsp; 1.1.4 | Enter **'John Doe Demo Teamspace'** (1) as the **Teamspace name**. Make sure the **Teamspace template** is **FC Hiring Teamspace Template** (2) and then click **Select Users** (3). <br/><img src="./images/Script4.png" width="800" /> |
| **Narration** | Once it is created, the HR manager provides teamspace access to the hiring and payroll managers so they can collaborate during the candidate's evaluation. |
| **Action** &nbsp; 1.1.5 | Click **Add Users and Groups...**<br/><img src="./images/Script5.png" width="800" /> |
| **Action** &nbsp; 1.1.6 | Type **debby** in the search area (1) and click the **magnifier** icon (2).<br/><img src="./images/Script6.png" width="800" /> |
| **Action** &nbsp; 1.1.7 | Select **debby** (1), who is the hiring manager, and click the **right-facing arrow** (2) to move her from the **Available** list to the **Selected** list.<br/><img src="./images/Script7.png" width="800" /> |
| **Action** &nbsp; 1.1.8 | Repeat the previous steps to add **patrick**, the payroll manager, to the **Selected** list (1). Click **OK** (2). <br/><img src="./images/Script8.png" width="800" /> |
| **Action** &nbsp; 1.1.9 | Select **Member** (1) in the **Roles** menu and click **Add** (2).<br/><img src="./images/Script9.png" width="800" /> |
| **Action** &nbsp; 1.1.10 | Click **Finish**.<br/><img src="./images/Script10.png" width="800" /> |

| **1.2** | **Add files to share** |
| :--- | :--- |
| **Narration** | The HR manager created the applicant’s new teamspace based on Focus Corp's 'FC Hiring Teamspace' template. When a new teamspace is created using this template, it includes all the forms that need to be completed and submitted for each candidate. |
| **Action** &nbsp; 1.2.1 | Click the **HR Documents** folder. <br/><img src="./images/Script11.png" width="800" /> |
| **Action** &nbsp; 1.2.2 | Point out that the **HR Documents** folder is now open and the necessary documents are now available.<br/><img src="./images/Script12.png" width="800" /> |
| **Narration** | The HR manager uses the HR document template to create copies that are specific to the applicant. When he does this in the teamspace, the documents are automatically shared with the rest of the hiring team.<br/>The content management software applies the role-based access restrictions configured in the FC Hiring Teamspace template, which specifies the permissions granted to each team member. |
| **Action** &nbsp; 1.2.3 | Click the **Candidate files** folder. <br/><img src="./images/Script13.png" width="800" /> |
| **Narration** | The HR manager uploads the candidate's documents to the 'Candidate files' folder. He moves the files from his computer to the 'Candidate files' folder with a simple drag-and-drop. |
| **Action** &nbsp; 1.2.4 | Click the **John Doe Diploma.pdf** document and drag it from your local Documents folder to the **John Doe Demo Teamspace / Candidate files** folder in IBM Navigator. <br/><img src="./images/Script14.png" width="800" /> |
|**Narration** | When the HR manager moves the files, a document entry form enables him to enter the required metadata.<br/>Focus Corp’s content administrator had previously worked with HR to define the metadata to include with files that are added to the teamspace. This metadata can be used later to quickly identify, classify, or search for a document. |
|**Action** &nbsp; 1.2.5 | Enter **'John Doe'** as the **Candidate Name**  (1) and select **Diploma** as the **Document Type** (2). Select **External** for **Document Source** (3). This indicates that the document originated outside of Focus Corp.<br/>Select **R&D** for the **Department Name** (4) and set the **Application date** to the date 3 days in the future (5). Click **Add** (6).<br/><img src="./images/Script15.png" width="800" /> |
|**Narration** | In the navigate view, team members can now add comments to the file, ‘like’ the file, or add the file to their favorites. |
|**Action** &nbsp; 1.2.6 | Click the **navigate view** icon. <br/><img src="./images/Script16.png" width="800" /> |
|**Action** &nbsp; 1.2.7 | Select the **John Doe Diploma.pdf** row. <br/><inline-notification text="Be sure to click within the row’s white space (not the document name). "></inline-notification><br/><img src="./images/Script17.png" width="800" /> |
|**Action** &nbsp; 1.2.8 | Point out the **document-related actions and information** (1), pre-defined **Properties** (2), and the **star** icon that adds the file to favorites (3).<br/><img src="./images/Script18.png" width="800" /> |
|**Narration** | The candidate had previously submitted a video detailing his professional qualifications, strengths and weaknesses. The HR manager adds the video to the content management system. |
|**Action** &nbsp; 1.2.9 | Move the **John Doe Video.mp4** file to the **Candidate files** folder.<br/><img src="./images/Script19.png" width="800" /> |
|**Action** &nbsp; 1.2.10 | Enter **'John Doe'** as the **Candidate Name** (1) and select **Candidate Video** as the **Document Type** (2). Select **External** for **Document Source** (3). <br/>Select **R&D** for the **Department Name** (4) and set the **Application date** to the date 3 days in the future (5). Click **Add** (6).<br/><img src="./images/Script20.png" width="800" /> |
|**Action** &nbsp; 1.2.11 | Click **John Doe Video.mp4**.<br/><img src="./images/Script21.png" width="800" /> |
|**Narration** | The hiring team wanted to quickly review specific candidate responses within the submitted video. The HR manager bookmarks the video, which allows hiring team members to go directly to the sections of the video they would like to see. |
|**Action** &nbsp; 1.2.12 | Click **Bookmarks**.<br/><img src="./images/Script22.png" width="800" /> |
|**Action** &nbsp; 1.2.13 | Click **New Bookmark**.<br/><img src="./images/Script23.png" width="800" /> |
|**Narration** | The HR manager adds bookmarks to the video to make it easier to find the individual responses. |
|**Action** &nbsp; 1.2.14 | Enter **Overview** (1) as the bookmark name, enter '**Tell me about yourself?**' (2) in the bookmark description and click **OK** (3). <br/><img src="./images/Script24.png" width="800" /> |
|**Action** &nbsp; 1.2.15 | Close the IBM Navigator Viewer window. |
|**Narration** | The HR manager bookmarks the remaining sections of the video and adds the applicant’s other documents to his candidate file. <br/>Let’s jump ahead and see the teamspace with all the documents added. |
|**Action** &nbsp; 1.2.16 | Click **x** to close the **John Doe Demo Teamspace**. <br/><img src="./images/Script25.png" width="800" /> |
|**Action** &nbsp; 1.2.17 | Click **John Doe**. <br/><img src="./images/Script26.png" width="800" /> |
|**Action** &nbsp; 1.2.18 | Click **Candidate files**.<br/><img src="./images/Script27.png" width="800" /> |
|**Action** &nbsp; 1.2.19 | Click the **Magazine view** icon. <br/><img src="./images/Script28.png" width="800" /> |
|**Narration** | Now the hiring team can collaborate on the applicant’s documents. |

| **1.3** | **Manage role-based redactions** |
| :--- | :--- |
| **Narration** | To adhere to Focus Corp's privacy guidelines, HR must prevent unauthorized access to the applicant’s personal information, such as his home address. <br/>The HR manager uses role-based redactions to automatically mask sensitive information, based on each user's role. The role-based access capabilities enable Focus Corp to explicitly define who has permission to see the redacted information. <br/>The HR manager starts by validating that the role-based redactions have been set correctly by the content administrator. |
|**Action** &nbsp; 1.3.1 | Click the **hamburger** icon to open the IBM Navigator menu.<br/><img src="./images/Script40.png" width="800" /> |
| **Narration** | The HR manager uses the Administration menu to review and update the role-based access. |
|**Action** &nbsp; 1.3.2 | Click **Administration.** <br/><img src="./images/Script41.png" width="800" /> |
|**Action** &nbsp; 1.3.3 | Click **Role-based Redactions**. <br/><img src="./images/Script42.png" width="800" /> |
| **Narration** | The HR manager reads through the 'Private Information' redaction policy, which specifies who can see a candidate's private information. |
|**Action** &nbsp; 1.3.4 | Double-click **Private Information**. <br/><img src="./images/Script43.png" width="800" /> |
|**Action** &nbsp; 1.3.5 | Click **Policies and Roles**. <br/><img src="./images/Script44.png" width="800" /> |
|**Action** &nbsp; 1.3.6 | If prompted, enter the **User name ‘cp4admin’** and the **Password** (1) from your cheat sheet. Click **Log In** (2).<br/><img src="./images/Script45.png" width="800" /> |
| **Narration** | The 'Private Information' reason contains two redaction roles: editors and viewers. *Editors* can add or remove redactions. *Viewers* can see redacted information but cannot change it. No other users can view redacted information. |
|**Action** &nbsp; 1.3.7 | Scroll down (1) and point out the payroll manager’s role as a **FC Redaction viewer** (2). <br/><img src="./images/Script47.png" width="800" /> |
| **Narration** | The HR manager verifies that only Patrick, the payroll manager, can view private information. Other members of the hiring team, such as the hiring manager, will not be able to access the redacted information. <br/>Confident that these settings are correct, the HR manager is ready to redact the documents. |
|**Action** &nbsp; 1.3.8 | Click the **hamburger** icon.<br/><img src="./images/Script48.png" width="800" /> |
|**Action** &nbsp; 1.3.9 | Click **Teamspaces**.<br/><img src="./images/Script49.png" width="800" /> | 
|**Action** &nbsp; 1.3.10 | Click **John Doe**.<br/><img src="./images/Script341.png" width="800" /> |
|**Action** &nbsp; 1.3.11 | Click **Candidate files**.<br/><img src="./images/Script342.png" width="800" /> |
| **Narration** | The HR manager opens the applicant’s resume, selects the information to redact, and indicates it is private information. |
|**Action** &nbsp; 1.3.12 | Click **John Doe Resume.pdf** to open it in the document viewer.&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  <br/><img src="./images/Script29.png" width="800" /> |
|**Action** &nbsp; 1.3.13 | Click the **redaction** icon, which is a darkened rectangle. &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<br/><img src="./images/Script30.png" width="800" /> |
|**Action** &nbsp; 1.3.14 | Redact the applicant’s email address, phone number and home address by drawing a rectangle around them using the redaction tool. <br/><img src="./images/Script31.png" width="800" /> <br/><inline-notification text="Make sure the black rectangle does not overlap the blue area above the hidden text. The rectangle should be minimal. <br/> <img src='https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-managing-and-securing-enterprise-content-at-scale/images/Prep-1-3-14-Note.png' width='600' /> "></inline-notification> <br/> |
|**Action** &nbsp; 1.3.15 | Right-click the **redaction rectangle** (1) and click the **document redaction reason** icon (2).&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <br/><img src="./images/Script32.png" width="800" /> |
|**Action** &nbsp; 1.3.16 | Select **Private Information** as the redaction reason (1) and click **OK** (2). &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <br/><img src="./images/Script33.png" width="800" /> |
| **Narration** | This hides the applicant’s personal information from users who do not have viewing rights. The hiring manager does not have viewing rights to this information and will not be able to see it.<br/>The HR manager acknowledges they have reviewed and verified the applicant's details by adding a notation on the document. |
|**Action** &nbsp; 1.3.17 | Click the **stamp** icon (1) and select the **Approved user date** stamp (2).&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <br/><img src="./images/Script34.png" width="800" /> |
| **Narration** | The HR manager uses a pre-defined annotation to indicate he has verified the applicant meets specific job criteria.<br/> |
|**Action** &nbsp; 1.3.18 | Click above the name on the document to add the annotation. &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<br/><img src="./images/Script35.png" width="800" /> |
| **Narration** | The HR manager changes the notation color to indicate that the applicant is eligible for a face-to-face interview.&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
|**Action** &nbsp; 1.3.19 | Right-click the **annotation** (1), select the **text color** icon (2), and select **orange** (3).<br/><img src="./images/Script36.png" width="800" /> |
|**Action** &nbsp; 1.3.20 | Click the **x** to close the color selector view (1) and click anywhere in the document to close the menu (2). &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<br/><img src="./images/Script37.png" width="800" /> |
|**Action** &nbsp; 1.3.21 | Click the **save** icon and close the IBM Navigator Viewer window. &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <br/><img src="./images/Script38.png" width="800" /> |
|**Action** &nbsp; 1.3.22 | Click the **user** icon (1) and click **Log Out** (2) to exit IBM Navigator.<br/><img src="./images/Script39.png" width="800" /> |
 
<br/>

**[Go to top](#top)**

</details>

<span id="spanID"></span>
<details markdown="1">

<summary>2 - Accessing and viewing content</summary>

<br/>

| **2.1** | **View documents in a teamspace** |
| :--- | :--- |
| **Narration** | The hiring manager needs to learn more about the applicant. She reviews the documents shared by HR. |
| **Action** &nbsp; 2.1.1 | Sign into IBM Navigator using the hiring manager’s credentials:<br/>**Username: debby** and **Password: debby** (1). Click **Log in** (2). <br/><img src="./images/Script113.png" width="800" /> |
| **Action** &nbsp; 2.1.2 | Click the **Teamspaces** tile. <br/><img src="./images/Script2.png" width="800" /> |
| **Action** &nbsp; 2.1.3 | Select the **John Doe** teamspace. <br/><img src="./images/Script114.png" width="800" /> |
| **Action** &nbsp; 2.1.4 | Click **Candidate files**. <br/><img src="./images/Script115.png" width="800" /> | 
| **Narration** | The hiring manager reviews the applicant’s resume. |
| **Action** &nbsp; 2.1.5 | Click the **Magazine view** icon. <br/><img src="./images/Script116.png" width="800" /> |  
| **Action** &nbsp; 2.1.6 | **Select the John Doe Resume.pdf** row.<br/><inline-notification text="Be sure to click within the row’s white space (not the document name). "></inline-notification><br/><img src="./images/Script117.png" width="800" /> |  
| **Narration** | The hiring manager confirms that the metadata required by her department is pre-populated in the properties section. She is not authorized to view the applicant’s personal information, so it is concealed in the document preview thumbnail. |
| **Action** &nbsp; 2.1.7 | Review the **Properties** section (1) and point out that the address information is redacted in the hiring manager’s **thumbnail** view (2). <br/><img src="./images/Script118.png" width="800" /> | 
| **Action** &nbsp; 2.1.8 | Click **John Doe Resume.pdf**.<br/><img src="./images/Script119.png" width="800" /> | 
| **Action** &nbsp; 2.1.9 | Scroll down to show the resume.<br/><img src="./images/Script120.png" width="800" /> | 
| **Narration** | The hiring manager reviews the details of the resume. The candidate is applying for a position that often works with a team in France. Therefore, a working knowledge of French is required for the job.<br/>She adds an annotation to assess the applicant's French language skills. |
| **Action** &nbsp; 2.1.10 | Click the **sticky note** icon (1) and then click next to the **SPOKEN LANGUAGES** section (2).<br/><img src="./images/Script121.png" width="800" /> | 
| **Action** &nbsp; 2.1.11 | Type **'Evaluate the candidate’s French language skills.**' (1) and click **Update** (2).<br/><img src="./images/Script122.png" width="800" /> | 
| **Action** &nbsp; 2.1.12 | Click the **save** icon.<br/><img src="./images/Script123.png" width="800" /> | 
| **Action** &nbsp; 2.1.13 | Close the IBM Navigator Viewer window. |
| **Narration** | The hiring manager 'likes' the resume and adds it to her favorites so she can compare the finalists later. |
| **Action** &nbsp; 2.1.14 | Click the **thumbs-up** icon (1) to 'like' the file. Click the **star** icon (2) to add the resume to favorites. <br/><img src="./images/Script202.png" width="800" /> | 
| **Narration** | To help decide whether to move forward with an interview, the hiring manager watches a few specific sections of the applicant’s video. |
| **Action** &nbsp; 2.1.15 | Click **John Doe Video.mp4.** <br/><img src="./images/Script50.png" width="800" /> | 
| **Narration** | She uses bookmarks in the applicant's video to skip directly to responses she’s interested in. Many applicant videos are over 20 minutes. The bookmark feature saves her time by letting her focus on specific parts of the video. |
| **Action** &nbsp; 2.1.16 | Click **Bookmarks** to open the bookmarks menu. <br/><img src="./images/Script51.png" width="800" /> | 
| **Action** &nbsp; 2.1.17 | Select the **Weaknesses** bookmark and wait for the video to load.<br/><img src="./images/Script52.png" width="800" /> | 
| **Action** &nbsp; 2.1.18 | Click the **play** icon and watch both the Weaknesses and Strengths sections. Close the IBM Navigator viewer when you are done.<br/><img src="./images/Script53.png" width="800" /> | 
| **Action** &nbsp; 2.1.19 | Close the **IBM Navigator Viewer** window.
| **Narration** | The hiring manager decides to interview the applicant. She lets the HR team know to schedule an interview by tagging the applicant’s resume with the word ‘selected'. |
| **Action** &nbsp; 2.1.20 | Click **Tags** in the **John Doe Resume.pdf **row. <br/><img src="./images/Script54.png" width="800" /> | 
| **Action** &nbsp; 2.1.21 | Write '**selected**' and hit enter on your keyboard.<br/><img src="./images/Script55.png" width="800" /> | 
| **Action** &nbsp; 2.1.22 | Click **Close**. <br/><img src="./images/Script56.png" width="800" /> | 
| **Narration** | The hiring team schedules the interview. To prepare, the hiring manager reviews the content she previously 'favorited'. |
| **Action** &nbsp; 2.1.23 | Click **IBM Navigator**.<br/><img src="./images/Script201.png" width="800" /> | 
| **Action** &nbsp; 2.1.24 | Click the **Content Favorites** tile.<br/><img src="./images/Script57.png" width="800" /> | 
| **Action** &nbsp; 2.1.25 | Double-click **John Doe Resume.pdf**.<br/><img src="./images/Script58.png" width="800" /> | 
| **Action** &nbsp; 2.1.26 | Scroll down to the **sticky note** (1) and hover your mouse over the note (2).<br/><img src="./images/Script59.png" width="800" /> | 
| **Narration** | She looks over the resume and annotations. The sticky note reminds her she must evaluate the candidate's French language skills. |
| **Action** &nbsp; 2.1.27 | Point out the annotation.<br/><img src="./images/Script60.png" width="800" /> | 
| **Action** &nbsp; 2.1.28 | Close the IBM Navigator Viewer window. |

<br/>

**[Go to top](#top)**

</details>

<span id="spanID"></span>
<details markdown="1">

<summary>3 - Annotating and merging documents</summary>

<br/>

| **3.1** | **Edit and add content** |
| :--- | :--- |
| **Narration** | The hiring manager needs to capture interview feedback on the candidate evaluation form. She downloads the form from Teamspace’s document templates. |
| **Action** &nbsp; 3.1.1 | Click **Teamspaces**.<br/><img src="./images/Script61.png" width="800" /> | 
| **Action** &nbsp; 3.1.2 | Click **HR Documents**.<br/><img src="./images/Script62.png" width="800" /> | 
| **Narration** | The filmstrip view helps the hiring manager see the available HR documents. She chooses the 'Evaluation form' and creates a copy in the applicant’s Candidate files folder. |
| **Action** &nbsp; 3.1.3 | Click the **Filmstrip view** icon.<br/><img src="./images/Script63.png" width="800" /> | 
| **Action** &nbsp; 3.1.4 | Click the first document on the bottom left of the filmstrip viewer.<br/><img src="./images/Script64.png" width="800" /> | 
| **Action** &nbsp; 3.1.5 | Scroll right until you see the **FC Evaluation form** in the viewer.<br/><img src="./images/Script65.png" width="800" /> | 
| **Action** &nbsp; 3.1.6 | Click **Actions** (1), then click **Folders** (2). Select **Add to Folder** (3).<br/><img src="./images/Script66.png" width="800" /> | 
| **Action** &nbsp; 3.1.7 | Select **Candidate files** (1) and click **Add** (2).<br/><img src="./images/Script67.png" width="800" /> | 
| **Action** &nbsp; 3.1.8 | Click the **details view** icon (1) and click **Candidate files** (2).<br/><img src="./images/Script68.png" width="800" /> | 
| **Narration** | The hiring manager opens the evaluation form directly from the applicant’s teamspace files so she can edit the form during the interview. |
| **Action** &nbsp; 3.1.9 | Click **Refresh** (1) and then Click **FC Evaluation form.docx**.<br/><img src="./images/Script69.png" width="800" /> | 
| **Narration** | The hiring manager switches to permanent redaction mode, which ‘hard codes’ her updates to the document for every subsequent viewer. |
| **Action** &nbsp; 3.1.10 | Click the **permanent redaction mode marker** icon.<br/><img src="./images/Script70.png" width="800" /> | 
| **Action** &nbsp; 3.1.11 | Click **New Version**. <br/><img src="./images/Script71.png" width="800" /> <br/>The fillable version of the candidate evaluation form displays.<br/><img src="./images/Script72.png" width="800" /> |  
| **Action** &nbsp; 3.1.12 | Return to the IBM Navigator view window. Point out the **lock** icon. <br/><img src="./images/Script73.png" width="800" /> |
| **Narration** | While the hiring manager edits the document, it is locked to prevent anyone else from making edits. |
| **Action** &nbsp; 3.1.13 | Return to the candidate evaluation form, click the **text** icon (1), and then select the free text field under **Candidate Name** (2).<br/><img src="./images/Script74.png" width="800" /> |
| **Narration** | She adds the candidate’s name and changes the text color to blue to highlight it. |
| **Action** &nbsp; 3.1.14 | Type '**John Doe**' (1) and click the **font color** icon (2).<br/><img src="./images/Script75.png" width="800" /> |
| **Action** &nbsp; 3.1.15 | Select blue.<br/><img src="./images/Script76.png" width="800" /> |
| **Action** &nbsp; 3.1.16 | Close the **color selector view** (1) and click the **checkmark** (2) to accept the annotation changes.  <br/><img src="./images/Script77.png" width="800" /> |
| **Narration** | The hiring manager needs to capture the date and time to ensure compliance with regulatory rules. She uses the annotation tools to add these details to the form. | 
| **Action** &nbsp; 3.1.17 | Click the **stamp** icon (1), select **date time** (2), and click in the free text area under **Date & Time** (3). <br/><img src="./images/Script78.png" width="800" /> |
| **Action** &nbsp; 3.1.18 | Click the date annotation.<br/><img src="./images/Script79.png" width="800" /> |
| **Action** &nbsp; 3.1.19 | Click the color icon, select blue, close the color selector and validate the update (as done previously in steps 3.1.14-16). |
| **Narration** | At the end of the interview, the hiring manager saves the document with her edits. |
| **Action** &nbsp; 3.1.20 | Click **Redact.** <br/><img src="./images/Script80.png" width="800" /> |
| **Action** &nbsp; 3.1.21 | Wait for the redaction to complete. Close IBM Navigator Viewer window. |
| **Narration** | The document thumbnail is updated to reflect the hiring manager’s changes. The document is automatically unlocked so other team members can now edit it. |
| **Action** &nbsp; 3.1.22 | Point out that the **FC Evaluation form preview thumbnail** is updated (1) and the document is no longer **locked** (2). <br/><img src="./images/Script82.png" width="800" /> |
| **Action** &nbsp; 3.1.23 | Drag and drop **John Doe evaluation form.pdf** to the **Candidate files** folder.<br/><img src="./images/Script83.png" width="800" /> |
| **Narration** | The hiring manager must add the required metadata to meet departmental standards. |
| **Action** &nbsp; 3.1.24 | Enter '**John Doe**' as the **Candidate Name** (1) and select **Evaluation form ** as the **Document Type** (2).<br/>Select **R&D** for the **Department Name** (3) and set the **Application date** to the current date (4). Click **Add** (5).<br/><img src="./images/Script84.png" width="800" /> |
| **Action** &nbsp; 3.1.25 | Show that a copy of the **Evaluation form** is added (1). **Log Out** of IBM Navigator (2).<br/><img src="./images/Script85.png" width="800" /> |
 
| **3.2** | **Merge documents** |
| :--- | :--- |
| **Narration** | The hiring manager has decided to make an offer to the applicant. <br/>The HR manager suggests a salary based on the feedback added to the salary discussion form. He needs to get approval for the salary from both the hiring and payroll managers. |
| **Action** &nbsp; 3.2.1 | Sign into IBM Navigator using **Username: henry** and **Password: henry** (1). Click **Log in** (2).<br/><img src="./images/Script86.png" width="800" /> |
| **Action** &nbsp; 3.2.2 | Click the **Teamspaces** tile.<br/><img src="./images/Script2.png" width="800" /> |
| **Action** &nbsp; 3.2.3 | Select the **John Doe** Teamspace.<br/><img src="./images/Script87.png" width="800" /> |
| **Action** &nbsp; 3.2.4 | Click **Candidate files**.<br/><img src="./images/Script88.png" width="800" /> |
| **Action** &nbsp; 3.2.5 | Drag the **John Doe salary discussion form.pdf** from your local documents to the **Candidates files** folder in IBM Navigator.<br/><img src="./images/Script89.png" width="800" /> |
| **Action** &nbsp; 3.2.6 | Enter '**John Doe**' as the **Candidate Name** (1) and select **HR Process** as the **Document Type** (2).<br/>Select **R&D** for the **Department Name** (3) and set the **Application date** to the current date (4). Click **Add** (5).<br/><img src="./images/Script90.png" width="800" /> |
| **Narration** | The HR manager merges the second page from the evaluation form, and the salary discussion form, into a single document to simplify the salary approval. |
| **Action** &nbsp; 3.2.7 | Click **John Doe Evaluation form.pdf**.<br/><img src="./images/Script91.png" width="800" /> |
| **Action** &nbsp; 3.2.8 | Click **Merge and Split** at the top right of the viewer.<br/><img src="./images/Script92.png" width="800" /> |
| **Action** &nbsp; 3.2.9 | Return to **Candidate files** and click **John Doe Salary discussion form.pdf**.  <br/><img src="./images/Script93.png" width="800" /> <br/>The final merge and split interface should match the view below:<br/> <img src="./images/Script95.png" width="800" />  | 
| **Narration** | Now that the documents are added to the ‘merge and split’ tool, the HR manager creates a summary document by merging the pages required for salary approval. |
| **Action** &nbsp; 3.2.10 | Click the **+** icon to create a new document.<br/><img src="./images/Script96.png" width="800" /> | 
| **Action** &nbsp; 3.2.11 | Right-click on the **New Document** tab (1) and select **Rename** (2).<br/><img src="./images/Script97.png" width="800" /> | 
| **Action** &nbsp; 3.2.12 | Enter ‘**John Doe Merged summary**’.<br/><img src="./images/Script98.png" width="800" /> | 
| **Narration** | First, he adds the second page of the evaluation form. |
| **Action** &nbsp; 3.2.13 | Click the **John Doe Evaluation form.pdf** tab.<br/><img src="./images/Script203.png" width="800" /> | 
| **Action** &nbsp; 3.2.14 | Click the **second page of the document** (1) in the thumbnail viewer. Click the **copy** icon (2) and click the **John Doe Merged summary.pdf** tab (3) to return to the new document.<br/><img src="./images/Script103.png" width="800" /> | 
| **Action** &nbsp; 3.2.15 | Click the **paste** icon.<br/><img src="./images/Script104.png" width="800" /> | 
| **Narration** | Then he adds the salary discussion form. |
| **Action** &nbsp; 3.2.16 | Click the **John Doe Salary discussion form.pdf** tab.<br/><img src="./images/Script105.png" width="800" /> | 
| **Action** &nbsp; 3.2.17 | Click the **copy** icon.<br/><img src="./images/Script107.png" width="800" /> | 
| **Action** &nbsp; 3.2.18 | Click the **John Doe Merged summary.pdf** tab.<br/><img src="./images/Script108.png" width="800" /> | 
| **Action** &nbsp; 3.2.19 | Click the **paste** icon.<br/><img src="./images/Script109.png" width="800" /> | 
| **Narration** | He now saves the document and fills in the required properties to add it to the applicant’s candidate files folder. |
| **Action** &nbsp; 3.2.20 | Click the **add document** icon.<br/><img src="./images/Script110.png" width="800" /> | 
| **Action** &nbsp; 3.2.21 | Enter '**John Doe**' as the **Candidate Name** (1) and select **HR process** as the **Document Type** (2). <br/>Select **R&D** for the **Department Name** (3), set the **Application date** to the current date (4). Click **Add** (5).<br/><img src="./images/Script111.png" width="800" /> | 
| **Action** &nbsp; 3.2.22 | Close the IBM Navigator Viewer. |
| **Action** &nbsp; 3.2.23 | Select the new **John Doe Merged summary.pdf** document.<br/><inline-notification text="Be sure to click within the row’s white space (not the document name)."></inline-notification><br/><img src="./images/Script112.png" width="800" /> | 
| **Narration** | The merged document is now ready to be approved by the stakeholders. |

<br/>

**[Go to top](#top)**

</details>

<span id="spanID"></span>
<details markdown="1">

<summary>4 - Managing the document approval process </summary>

<br/>

| **4.1** | **Launch a validation process** |
| :--- | :--- |
| **Narration** | The HR manager needs hiring stakeholders to approve the salary offer. <br/>Using the built-in document approval workflow, he routes the salary request to the hiring manager for approval. Once she approves, the request will automatically proceed to the payroll manager for his final approval. |
| **Action** &nbsp; 4.1.1 | Select the **John Doe Merged summary.pdf** row (1). Then click **Actions** (2), select **Workflow** (3), and click **Launch Workflow** (4). <br/><img src="./images/Script301.png" width="800" /> | 
| **Action** &nbsp; 4.1.2 | Select **Sequential review** in the **Name** dropdown list (1) and click **Launch** (2).<br/><img src="./images/Script302.png" width="800" /> | 
| **Narration** | The HR manager specifies Debby, the hiring manager, as the first approver. |
| **Action** &nbsp; 4.1.3 | Click the **downward arrow** to expand the **Reviewers** dropdown list.<br/><img src="./images/Script303.png" width="800" /> | 
| **Action** &nbsp; 4.1.4 | Type '**debby**' (1) and click the **magnifier** icon (2).<br/><img src="./images/Script304.png" width="800" /> | 
| **Action** &nbsp; 4.1.5 | Click the **right-facing arrow** to move the userid **debby** from the **Available** list to the **Selected** list. <br/><img src="./images/Script305.png" width="800" /> | 
| **Narration** | Now the HR manager adds Patrick, the payroll manager, to the approval process. |
| **Action** &nbsp; 4.1.6 | Repeat the previous step to add **patrick** to the **Selected list** (1). Click **OK** (2). <br/><img src="./images/Script306.png" width="800" /> | 
| **Narration** | Next, the HR manager sets a due date for the approvers to respond with their approvals. |
| **Action** &nbsp; 4.1.7 | Click the **date selector** to select a date approximately three business days from the current date.<br/><img src="./images/Script307.png" width="800" /> | 
| **Narration** | The HR manager adds instructions for the approvers, validates that the salary discussion document is attached to the message, and launches the salary approval workflow. |
| **Action** &nbsp; 4.1.8 | Enter '**Please approve or reject the attached salary request document, and add any comments.**' in the **Instructions for reviewers** field (1). Click the **Attachments** tab (2).<br/><img src="./images/Script308.png" width="800" /> | 
| **Action** &nbsp; 4.1.9 | Point out that the **John Doe Merged summary.pdf** is automatically attached (1). Click **Launch Workflow** (2).<br/><img src="./images/Script309.png" width="800" /> | 
| **Action** &nbsp; 4.1.10 | Click the **user** icon (1) and click **Log Out** (2).<br/><img src="./images/Script310.png" width="800" /> | 
  
| **4.2** | **Review work items** |
| :--- | :--- |
| **Narration** | The hiring manager is notified that she needs to approve the salary request. She logs in to review the request. <br/>In a real implementation, the notification would include a link to access the approval form. For this demonstration, we are showing a version that does not require setting up outside email accounts to demonstrate this functionality.<br/>If she approves the request, a notification will automatically be sent to the payroll manager for his approval. |
| **Action** &nbsp; 4.2.1 | Sign into IBM Navigator using the hiring manager’s credentials:<br/>**Username: debby** and **Password: debby** (1). Click **Log in** (2).<br/><img src="./images/Script311.png" width="800" /> | 
| **Action** &nbsp; 4.2.2 | Click the **Work** tile.<br/><img src="./images/Script312.png" width="800" /> | 
| **Action** &nbsp; 4.2.3 | Select the **Review for John Doe Merged summary.pdf** row (1) and click **Open** (2).<br/><img src="./images/Script313.png" width="800" /> | 
| **Narration** | The hiring manager opens the notification. She sees the request for salary approval, the requester name, and the due date. |
| **Action** &nbsp; 4.2.4 | Point out the process details (1) and click the **Attachments** tab (2). <br/><img src="./images/Script314.png" width="800" /> |  
| **Action** &nbsp; 4.2.5 | Click the **John Doe Merged summary.pdf**. <br/><img src="./images/Script315.png" width="800" /> |   
| **Narration** | The hiring manager reviews all the documents pertinent to the salary decision. She approves the requested salary. |
| **Action** &nbsp; 4.2.6 | Scroll down to show that the merged document includes the second page of the applicant’s evaluation form and the salary discussion form. <br/><img src="./images/Script316.png" width="800" /> |   
| **Action** &nbsp; 4.2.7 | Click the **stamp** icon (1) and select **Approved user date** (2). Click in the **Hiring Dept box** (3) to place the stamp. <br/><img src="./images/Script317.png" width="800" /> |   
| **Narration** | When the hiring manager approves, the stamp automatically generates her name and the approval date. |
| **Action** &nbsp; 4.2.8 | Click the **save** icon. <br/><img src="./images/Script319.png" width="800" /> |   
| **Action** &nbsp; 4.2.9 | Close the IBM Navigator Viewer window.  |  
| **Narration** | Now the hiring manager adds her comments. |
| **Action** &nbsp; 4.2.10 | Click the **Properties** tab. <br/><img src="./images/Script320.png" width="800" /> |  
| **Action** &nbsp; 4.2.11 | In the **Comments** dialogue box, enter **'Salary approved for John Doe.'** (1). Click **Approve** (2).<br/><img src="./images/Script321.png" width="800" /> |  
| **Narration** | After the hiring manager approves the salary, the request is automatically sent to the payroll manager. |
| **Action** &nbsp; 4.2.12 | **Log out** from IBM Navigator. |
| **Action** &nbsp; 4.2.13 | Sign back into IBM Navigator using the payroll manager’s credentials:<br/>**Username: patrick** and **Password: patrick** (1). Click **Log in** (2).<br/><img src="./images/Script322.png" width="800" /> |  
| **Narration** | When the payroll manager receives a notification to approve the salary request, he logs in to review the request. |
| **Action** &nbsp; 4.2.14 | Click the **Work** tile.<br/><img src="./images/Script323.png" width="800" /> |  
| **Action** &nbsp; 4.2.15 | Click **Open**.<br/><img src="./images/Script324.png" width="800" /> |  
| **Action** &nbsp; 4.2.16 | Click the **History** tab. <br/><img src="./images/Script325.png" width="800" /> |  
| **Narration** | The payroll manager sees that the hiring manager has approved the salary. He reviews the pertinent documents. |
| **Action** &nbsp; 4.2.17 | Click the **Attachments** tab. <br/><img src="./images/Script326.png" width="800" /> |  
| **Action** &nbsp; 4.2.18 | Click the **John Doe Merged summary.pdf**.<br/><img src="./images/Script327.png" width="800" /> |  
| **Narration** | The payroll manager adds his approval. |
| **Action** &nbsp; 4.2.19 | Scroll to the end of the document. Click the **stamp** icon (1) and select **Approved user date** (2). Click in the **Payroll** box (3) to add the stamp.<br/><img src="./images/Script328.png" width="800" /> |  
| **Action** &nbsp; 4.2.20 | Point out the payroll manager’s approval is added to the document.<br/><img src="./images/Script329.png" width="800" /> |  
| **Action** &nbsp; 4.2.21 | Click the **save** icon.<br/><img src="./images/Script330.png" width="800" /> |  
| **Action** &nbsp; 4.2.22 | Close the IBM Navigator Viewer. |  
| **Narration** | The payroll manager adds his comments to the approval. |
| **Action** &nbsp; 4.2.23 | Click the **Properties** tab. <br/><img src="./images/Script331.png" width="800" /> |  
| **Action** &nbsp; 4.2.24 | Enter '**Salary looks appropriate**.' in the **Comments** dialogue box (1). Click **Approve** (2). <br/><img src="./images/Script332.png" width="800" /> |  
| **Narration** | A notification is automatically sent to the HR manager stating that the workflow tasks are complete. |
| **Action** &nbsp; 4.2.25 | Log out from IBM Navigator. |
| **Narration** | The notification to the HR manager indicates the salary has been approved. He logs in and reviews the hiring team’s comments. |
| **Action** &nbsp; 4.2.26 | Sign back in as the HR manager using **Username: henry** and **Password: henry** (1). Click **Log in** (2). <br/><img src="./images/Script333.png" width="800" /> |  
| **Action** &nbsp; 4.2.27 | Click **Work**. <br/><img src="./images/Script334.png" width="800" /> |  
| **Action** &nbsp; 4.2.28 | Click **Open**. <br/><img src="./images/Script335.png" width="800" /> |  
| **Action** &nbsp; 4.2.29 | Point out the sequential steps in the **Summary** tab (1) and the comments in the **Comments** column (2). Click **Complete** (2).<br/><img src="./images/Script336.png" width="800" /> |  
| **Narration** | The HR manager reviews the comments made by the hiring and payroll managers. He does not see any further actions needed from the hiring or payroll managers, so the salary approval workflow is complete. <br/>The company is ready to send an offer letter to the applicant. |

<br/>

**[Go to top](#top)**

</details>

<span id="spanID"></span>
<details markdown="1">

<summary>Summary </summary><br/>

Today we saw how a company uses IBM’s enterprise content management platform to share and manage documents while maintaining security and adhering to regulations.

We used role-based capabilities to secure content by customizing document access. We used redaction to ensure compliance with privacy regulations. We saw how the platform’s integrated features, such as annotation, video bookmarking and document merging, helped make the team more productive.

IBM’s content management capabilities are used by our customers today to securely manage hundreds of thousands, or in some cases millions, of documents in their organizations.

Thank you for attending today’s presentation.

<br/>

**[Go to top](#top)**

</details>