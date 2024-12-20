---
title: Process and task mining <br/>Technical Sales Level 3 demo
layout: demoscript
banner: images/Script-banner.png
---

<span id="top"></span>

<details markdown="1">

<summary>Introduction</summary><br/>

Today we will look at how IBM’s process mining capabilities are used to discover and analyze business processes and identify areas for improvement. We will use a customer account closing example to showcase how process mining helps an organization meet regulatory requirements while also reducing process execution cost.

By using the data from enterprise applications, we’ll see how process mining discovers and analyzes processes as they actually are, not as we think -- or hope -- they might be.  We’ll use the analysis capabilities to find process deviations and bottlenecks. Task mining will give us a complete picture of the end-end-end process by incorporating work done at the desktop level.  We’ll then use simulation to predict the benefits of implementing process improvements before making any automation investments.

Let’s get started.

(Demo intro slides <a href="./files/Process and Task Mining Platinum Demo - Intro deck.pptx" target="_blank" rel="noreferrer">here</a>)

(Printer-ready PDF of demo script <a href="./files/Process and Task Mining Platinum Demo - PDF script.pdf" target="_blank" rel="noreferrer">here</a>)


**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>1 - Visualizing the process</summary>
<br/>

| **1.1** | **Introduce the process challenges** |
| :--- | :--- |
| **Narration** | Focus Bank is a regional bank that is not meeting its regulatory requirements. The bank is required to complete all account closure requests within fourteen days. The bank knows it is not achieving this requirement, but is not sure why. Additionally, the bank performed over 60,000 account closures per year and suspects it could reduce process execution costs. However, it is unsure where to start. |

| **1.2** | **Visualize the end-to-end process** |
| :--- | :--- |
| **Narration** | Analyzing processes in process mining starts with importing log files from the applications used in your business processes. Focus Bank’s account closing process uses a customer service system to take the customer’s request, a network access application to remove online access to the accounts and banking systems to liquidate and delete the account. |
| **Action** &nbsp; 1.2.1 | Show the **Data source** page within the Process mining workspace, which you opened during demo preparation. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/1-2-1.png" width="800" /> |
| **Narration** | Log files are uploaded from the Datasource tab. Process mining accepts CSV or XES files as a data source. An API is available to programmatically upload log files. Once the file is uploaded, it is mapped to the relevant data columns. There are three mandatory columns: Process ID, Activity, and Time. Process ID can be anything that uniquely identifies each process instance or case, such as request number, order number, etc. For deeper analysis, it is recommended to add up to sixty additional custom fields. This will provide richer context data about each case and enhance the analysis. <br/><br/> Now that the data is loaded, let’s look at how process mining provides an end-to-end view of the account closure process. |
| **Action** &nbsp; 1.2.2 | Click the **Model** tab (1), and click the **x** (2) to close the **View options** panel. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/1-2-2.png" width="800" /> |
| **Narration** | We are looking at the end-to-end process for Focus Bank’s account closure process. This is provided here in the Model view perspective. <br/><br/> The business data imported from Focus Bank’s applications is used to automatically create and visualize the end-to-end account closure process, including all activities and paths. The account closure process spans multiple departments and business applications, all from which process mining algorithms correlate business data. <br/><br/> The darker color of an activity box indicates the activity was performed more frequently. For example, removing online access to the account (here labeled 'BO Service Closure') is dark blue because it is performed for most account closures. The same with the process flow lines. The darker the flow lines, the more frequent the process path is followed. For example, the flow line from 'BO Service Closure' to 'Close Reservation' is performed frequently and therefore has a darker flow line. |


**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>2 - Analyzing the process</summary>
<br/>

| **2.1** | **Case variant analysis** |
| :--- | :--- |
| **Narration** | From this visualization, we’ll start to analyze the discovered process. First, we’ll look at the various process paths taken to complete each account closure request. We call this *case variant analysis*. |
| **Action** &nbsp; 2.1.1 | Click the **Variants** icon. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/2-1-1.png" width="800" /> |
| **Narration** | Each account closure request is called a case. A process variant is the unique path a case takes to complete the account closure process (from start to end). Here we see the list of unique process variants with the percentage each is followed. This shows which paths are most frequently followed. For example, the most frequently followed path is taken about 36% of the time. |
| **Action** &nbsp; 2.1.2 | Click the first variant (1). Click the **X** (2) to close the **Process variants** panel. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/2-1-2.png" width="800" /> |
| **Narration** | When we select the first process variant, the visualization updates to display the steps unique to that variant. This path is taking almost twenty days on average to complete each account closure request. The most frequent variant is not meeting our regulatory requirement to complete the account closure within fourteen days. |

| **2.2** | **Reference model analysis** |
| :--- | :--- |
| **Action** &nbsp; 2.2.1 | Click the **Conformance** icon. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/2-2-1.png" width="800" /> |
| **Narration** | We’ve completed our first view of process analysis. Let’s see how the account closure process behaves versus what was expected. <br/><br/> Process modeling and process mining tools complement each other very well. Focus Bank had previously mapped out the account closure process using IBM Blueworks Live, which is a cloud-based collaborative process modeling application. They published a reference model to define how they intended the process to be performed, but they had no way to compare the reference model against the real-world performance. They simply had to hope the process was being performed as intended. <br/><br/> Using the process mining tool, the bank imported their Business Process Modeling Notation (BPMN) model from IBM Blueworks Live. They compared the documented (reference) model to the actual (data-derived) model. |
| **Action** &nbsp; 2.2.2 | In the **Model conformance** panel, under **Model view options**, select **Reference model** to show the reference model (i.e., the BlueWorks Live model). Then, select **Data derived model** to show the data-driven model (i.e., the process mining model). Lastly, select **Compare both models**. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/2-2-2.png" width="800" /> |
| **Narration** | By selecting ‘Reference,’ we visualize the reference model. <br/><br/> By selecting ‘Data-derived,’ we visualize the data-derived model. The data-derived model looks more complex. There are differences between what people thought the process should be and what is really occurring. <br/><br/> By selecting ‘Compare,’ we visualize the differences between the two models. A red-highlighted box is an activity occurring during real-world process execution but not included in the reference process. We see there are five such activities highlighted in red. As detailed in the comparison chart on the right, all these activities: 1) add significant time to completing account closure, 2) add significant cost, and 3) occur with significant frequency. Most notable is the unexpected activity ‘Complete Account Removal.’ In the reference model, we expected to remove the account with the ‘BO Service Closure’ activity. However, the data-derived model shows that an additional step, ‘Complete Account Removal,’ was needed to complete over 8,000 account closure requests. <br/><br/> Activities and process flow lines that are only present in the reference model are shown using yellow boxes and arrows. Activities present in both models are displayed using blue boxes (dark or light blue depending on the frequency).  Black arrows indicate the process flow line is present in both models. <br/><br/> We also see the impact of time and cost on not following the reference model. When the reference model is followed, it takes about 18 days per case. When we don’t follow the reference model, it takes an average of over 26 days. |
| **Action** &nbsp; 2.2.3 | Return to the main screen by clicking the **Conformance** icon. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/2-2-3.png" width="800" /> |

| **2.3** | **Performance management** |
| :--- | :--- |
| **Narration** | Process mining provides various ways to analyze the performance of the account closure process. The primary dimensions to consider are time, cost, and rework. For each of these dimensions, Key Performance Indicators (KPIs) are defined and visualized in the analysis. |
| **Action** &nbsp; 2.3.1 | Click the **Eye** icon (1) to show the **View options** panel. Change the **View mode** to **Duration** (2). <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/2-3-1.png" width="800" /> |
| **Narration** | Let’s see how the account closure process is performing based on time. 'BO Service Closure' is one of the activities taking the most time within the process. On average it takes more than a week to complete the account closure process. Since almost every case flows through this activity, this is our fundamental process bottleneck. |
| **Action** &nbsp; 2.3.2 | Set **KPI palette** to **On**. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/2-3-2.png" width="800" /> |
| **Narration** | Next, let’s consider KPI measurement.  Defining KPIs for the process facilitates process analysis. KPIs for individual activity durations provide insights into whether actual durations are meeting expectations. <br/><br/> The KPI view indicates two of the average activity durations (highlighted in red) are not meeting expectations, including ‘BO Service Closure.’ In addition, one activity for account closure (highlighted in yellow) is at risk of not meeting expectations. |

<br/>

**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>3 - Generating a BPMN model</summary><br/>

| **3.1** | **BPMN generation** |
| :--- | :--- |
| **Narration** | Focus Bank generated a standard BPMN (Business Process Modeling Notation) diagram of the Account Closure process. Just like the other data-driven views, this model is generated from actual process data. |
| **Action** &nbsp; 3.1.1 | Click the **BPMN** tab and wait for the model to generate. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/3-1-1.png" width="800" /> |
| **Narration** | The account closure activities, swim lanes, decision points, and process flows are shown in the BPMN diagram. |

<br/>

**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>4 - Mining for rules</summary><br/>

| **4.1** | **Rules discovery** |
| :--- | :--- |
| **Narration** | Since the BPMN model was generated from actual account closure data, each decision point in the model has real data behind it. Clicking each decision box shows the results of what we refer to as rules discovery. |
| **Action** &nbsp; 4.1.1 | Click the **drop-down list** icon (1) next to **Create simulation**. Click **Discovery decision rules** (2). <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/4-1-1.png" width="800" /> |
| **Action** &nbsp; 4.1.2 | Click the decision gateway labeled **GW-XOR-19** (after **Liquidate Account**). <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/4-1-2.png" width="800" /> |
| **Narration** | For example, we can see why the account closure requires the extra step 'Make Adjustment.' It happens based on the status of the account closure request. <br/><br/> We can export the BPMN and decision mining rules to workflow and decision management tools, such as IBM Cloud Pak for Business Automation. |
| **Action** &nbsp; 4.1.3 | Click the **X** on the top right to close the **Gateway information** screen. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/4-1-3.png" width="800" /> |
| **Action** &nbsp; 4.1.4 | Click the **X** again to close the **Rules overview** screen. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/4-1-3-.png" width="800" /> |
| **Action** &nbsp; 4.1.5 | Click the **Model** tab. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/4-1-4.png" width="800" /> |

<br/>

**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>5 - Mining desktop tasks</summary><br/>

| **5.1** | **Task mining introduction** |
| :--- | :--- |
| **Narration** | Now, let’s focus on the bottleneck caused by the 'BO Service Closure' activity we found through the activity duration analysis. We identified the bottleneck but need more information to fully understand why it is happening. Task mining provides details of what is happening during the 'BO Service Closure' activity at the desktop level. <br/><br/> Task mining complements process mining by providing analysis of activities performed on an individual’s desktop. Task mining records, analyzes, and generates insights about user interactions with software applications. Think of task mining as replacing traditional time and motion studies. <br/><br/> We’re able to combine the server activity with the desktop activity to get a complete view of how the process is performed, including where specific individuals or teams are spending their time. This approach to process discovery helps identify opportunities for automation. <br/><br/> We can drill down into the 'BO Service Closure' activity to see the resources performing the activity. This table shows that the user group called 'BOC' is performing most of the work (96% of the time). |
| **Action** &nbsp; 5.1.1 | Click the **BO Service Closure** activity (1) and then the **Show activity statistics** icon (2). <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/5-1-1.png" width="800" /> |
| **Action** &nbsp; 5.1.2 | On the **Activity statistics** page, set the **View details for cases by** to **Resource**. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/5-1-1-.png" width="800" /> |
| **Narration** | In this case, we will want to record users in the 'BOC' group, since they perform this activity 96% of the time. If necessary, we could record multiple groups of users to complete our task mining analysis. Once the task mining data is recorded, it is integrated into the process flow discovered in the process mining model. |
| **Action** &nbsp; 5.1.3 | Close the **Activity statistics** screen by clicking the **X** on the top right. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/5-1-2.png" width="800" /> |
| **Action** &nbsp; 5.1.4 | Click the **Launch task mining process** icon. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/5-1-3.png" width="800" /> |
| **Narration** | A new window opens with the task mining view for the 'BO Service Closure' activity. All the capabilities we reviewed for process mining are available for task mining. We see the frequency of each step of the 'BO Service Closure' activity. These are the desktop steps needed to complete this activity, such as using the software applications and websites needed to close the account. |
| **Action** &nbsp; 5.1.5 | In the **View options** panel, under **Model view**, set the **View mode** to **Duration** (1). Click the **Variants** icon (2). <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/5-1-4.png" width="800" /> |
| **Narration** | We can view the variants for this activity.  The most frequent variant occurs just over 50% of the time.  Therefore, automating the first variant would impact at least half of the total account closures. |

| **5.2** | **Task mining analysis** |
| :--- | :--- |
| **Narration** | Next, let's perform a deeper analysis of the 'BO Service Closure' task. |
| **Action** &nbsp; 5.2.1 | Click the **Analytics** icon. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/5-2-1.png" width="800" /> |
| **Narration** | Analytic views, such as this one, can be created by business users and shared within your organization. As you discover and analyze new processes, you can create and share new views as needed. This level of analysis is used to determine the benefits, such as Return on Investment (ROI), that can be realized from automation. <br/><br/> The discovered task model and variants appear on the left. For each variant, we’ve discovered the individual subtasks that compose the ‘BO Service Closure’ task. <br/><br/> In the top center, we see ‘Productivity by Subtask.’ Each subtask time is composed of: <br/> • *Productive time*: Actual time spent on each specific subtask <br/> • *Idle time*: Time spent away from the desktop or not working on any monitored tasks <br/><br/> This analysis reveals the potential impact of how much time we would save from automation. It is quite common for analysts to base their ROI analysis on total subtask times because they do not realize or can’t measure the idle time and time spent on other tasks. With task mining, we have identified the actual time spent on a specific task as we build our business case for prioritization. |
| **Action** &nbsp; 5.2.2 | In the **Time Consumed by Application** panel at the bottom, hover within any of the activities to see the total time spent using the application. <br/><br/> <inline-notification text="Hover inside the bar on a particular color section. Highlight a single color, such as the blue or orange part. "></inline-notification> <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/5-2-3.png" width="800" /> |
| **Narration** | In the bottom center, the ‘Time Consumed by Application’ panel shows the time spent in the individual applications used to complete the ‘BO Service Closure’ task.  Each bar represents a software application broken down by the total time spent performing each activity. <br/><br/> We’ll exit the task mining view so we can move on to simulation. |
| **Action** &nbsp; 5.2.3 | Click the **Analytics** icon (1) and then **Processes** (2). <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/5-2-4.png" width="800" /> |
| **Action** &nbsp; 5.2.4 | Click **Processes**. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/5-2-5.png" width="800" /> |
| **Action** &nbsp; 5.2.5 | Click **Account Closure**. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/5-2-6.png" width="800" /> |

<br/>

**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>6 - Using simulation to optimize the process</summary>
<br/>

| **6.1** | **Simulation** |
| :--- | :--- |
| **Narration** | We identified opportunities to address the two main problems with the Account Closure process: (1) time to complete and (2) execution cost. Before acting, it is critical for the bank to understand the impact of planned changes and the expected outcome. The bank used simulation to predict the benefits of making changes to the process. |
| **Action** &nbsp; 6.1.1 | Click the **BPMN** tab (1) and then **Create simulation** (2). <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/6-1-1.png" width="800" /> |
| **Action** &nbsp; 6.1.2 | Provide a **Simulation title** [such as '**Account Closure**'] (1), and click **Create simulation** (2). <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/6-1-2.png" width="800" /> |
| **Narration** | As they consider possible process improvements, the bank compares the modified process to the currently executing process. This enables them to identify which changes would yield the greatest business benefits.  They are therefore able to validate the business case before making the investment to change the process. <br/><br/> The bank uses simulation to determine the impact of changes to individual activities and to the end-to-end process. They start with a simulation scenario that is pre-loaded with the historical account closure process data. From there, they change the simulation parameters, run the simulation, and compare the actual process to the simulated scenario. <br/><br/> For the 'Account Closure' process, the bank focuses on meeting the regulatory requirement of fourteen days to process account closure requests. Their previous analysis identifies that the main process bottleneck is the 'BO Service Closure' activity. |
| **Action** &nbsp; 6.1.3 | Scroll down to show different activities. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/6-1-3.png" width="800" /> |
| **Narration** | From here, the bank starts with historical process data and changes staffing levels, work hours, date ranges, etc. They could also filter by business data, such as region, to isolate or compare individual locations. |
| **Action** &nbsp; 6.1.4 | Scroll to the **BO Service Closure** activity. <br/><br/> Highlight the following: <br/> •	**Settings** – Change staff availability, total service time, and actual working time <br/> •	**Scheduling** – Change hours of operation <br/> •	**RPA** – Automate a task <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/6-1-4.png" width="800" /> |
| **Narration** | Using process mining, the bank identifies the bottleneck caused by the 'BO Service Closure' activity. They further identify, using task mining, that over 50% of the tasks for this activity follow the same steps to complete. They suspect the activity could be fully automated, due to the low number of task variants. They simulate the outcome of automating this step with RPA. |
| **Action** &nbsp; 6.1.5 | Select the **Robotic quote** tab and change the percentage of automation to **100%**. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/percentage.png" width="800" /> |
| **Action** &nbsp; 6.1.6 | Click **Run Simulation**. <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/6-1-6.png" width="800" /> <br/><br/> You will see the following simulation results: <br/> <img src="https://raw.githubusercontent.com/ibm-garage-tsa/platinum-demos/master/src/pages/300-business-automation-process-and-task-mining/images/6-1-6-.png" width="800" /> |
| **Narration** | The bank is now able see the results of making this change from the “as-is” model compared to the “to-be” model. With this new automation, the bank is expected to reduce the average end-to-end account closure time from about 21 days to under 13 days, while also reducing the average cost of each case. <br/><br/> The 'Case duration and count' chart shows the as-is process in blue and the simulated results in purple. In the simulated results (purple), the average service time is much lower and much more stable than the as-is results. The daily average number of active cases is also stable. This confirms the expected performance improvement when RPA is used to automate the ‘BO Service Closure’ activity. |

<br/>

**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>Summary</summary><br/>

Using a customer account closure example, we’ve shown how process mining is used to discover and analyze business processes and identify areas for improvement. Before process mining, the bank had very little knowledge of how to improve regulatory compliance or reduce cost. <br/><br/> The bank leveraged process mining to analyze the current process, including comparing the current process performance to their reference model. Next, they identified opportunities to alleviate the problems. They used task mining to drill down to the desktop activity level. Finally, they simulated how to use automation to get back into compliance and reduce overall costs.

Thank you for attending today's presentation.

<br/>

**[Go to top](#top)**

</details>
