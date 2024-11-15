---
title: Straight-through processing <br/>Technical Sales Level 3 demo
layout: demoscript
banner: images/Script-banner.png
---

<span id="top"></span>

<details markdown="1">

<summary>Introduction</summary><br/>

Welcome to the straight-through processing demonstration.

Today, I will demonstrate how the IBM Cloud Pak for Business Automation supports straight-through processing to automate customer refund requests quickly and easily. I’ll show how straight-through processing improves customer service by shortening turnaround times, while also reducing manual work.

This demo uses a customer refund example, but the same pattern can be applied to numerous business scenarios such as account opening, invoicing and claims processing.

We’ll show how line-of-business subject matter experts can use low-code tools that enable them to lead the implementation effort. We’ll see how decision management automates decisions that would otherwise be manual, and workflow manages exceptions and ensures the process stays on track when an exception occurs. We’ll also see how operational intelligence can provide visibility and insights that can be used to improve the process.

Let’s get started.

(Demo intro slides <a href="./files/Straight-through Processing Platinum Demo - Intro deck.pptx" target="_blank" rel="noreferrer">here</a>)

(Printer-ready PDF of demo script <a href="./files/Straight-through Processing Platinum Demo - PDF script.pdf" target="_blank" rel="noreferrer">here</a>)


**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>1 - Modeling the workflow</summary><br/>
<br/>

| **1.1** | **Introduce the refund request process without straight-through processing** |
| :--- | :--- |
| **Narration** | We will look at the process diagram for Focus Corp’s refund request process in Process Designer. Within this low-code environment, the process diagram will control the execution of each refund request. The process diagram adheres to the Business Process Model and Notation (BPMN) standard. We use drag-and-drop to build the process diagram from the palette on the right. This allows us to model the process steps and flow. From there, you can drill down to complete the implementation and testing of the process application. <br/> <br/> Looking at Focus Corp’s refund request process, customers can initiate returns directly from the company’s portal. Currently, each request is routed to a customer service agent for resolution. |
| **Action** &nbsp; 1.1.1 | Show the process diagram for Focus Corp’s **Request Refund without STP** (straight-through processing) in Process Designer, which you opened during your demo preparation. <br/> <img src="./images/Step_1_final_screen.png" width="800" /> |

<br/>

**[Go to top](#top)**

</details>
<span id="spanID"></span>
<a id="workplace"></a>
<details markdown="1">

<summary>2 - Executing the workflow without straight-through processing</summary><br/>
<inline-notification text="The first part of this section is for <strong>Workplace only</strong>. For <strong>Process Portal</strong>, please go <a href'#saas'>here</a>."></inline-notification><br/>

| **2.1** | **Task management and execution (Workplace)** |
| :--- | :--- |
| **Narration** | The customer service agent uses Workplace to work on their tasks. It is also used to launch processes and view the process dashboards. |
| **Action** &nbsp; 2.1.1 | Show the **Workplace** window that you opened during your preparation. <br/> <img src="./images/Stu_4.4.4_Self_install.png" width="800" /> |
| **Narration** | We are looking at the task list for the customer service agent. <br/> <br/> Workplace is highly customizable to fit your organization's look and feel. The responsive user interface provides flexibility to get work done anywhere, at any time, on any device type, from a desktop device in the office to a mobile device at home or at a customer site. It can be configured though a set of options without having to customize the Workplace application itself. <br/> <br/> Workplace has a robust search capability. You can create a customized task list, for example, with specific business data, by saving task-based searches for later use. <br/> <br/> Customer service agents use the task list to organize and work on the tasks assigned to them. Our agent received a new investigation task. |
| **Action** &nbsp; 2.1.2 | Click any **Refund Investigation Issue** task. If prompted, **Claim the task**. <br/> <img src="./images/Step_2.1_ROKS_action_3.png" width="800" /> |
| **Narration** | Once I open the task, I will have all the information needed to investigate the refund. |
| **Action** &nbsp; 2.1.3 | Click **Approve Refund**. <br/> <img src="./images/Step_2.1_ROKS_action_5.png" width="800" /> |
| **Narration** | Let’s review the request data and make an approval decision. Behind the scenes, the refund process is managed by workflow. Once the investigation task is completed, the system automatically updates Focus Corp’s ordering application and notifies the customer. <br/> <br/> Although the process is managed by workflow, there is currently no straight-through processing since every request must be examined by a customer service agent. Let’s go back to the process diagram and see how we can improve things with straight-through processing. |

<span id="spanID"></span>
<a id="saas"></a>
<details markdown="1">
The customer service agent uses Workplace to work on their tasks. It is also used to launch processes and view the process dashboards.
<summary>2a - Executing the workflow without straight-through processing (Process Portal only) </summary><br/>

<inline-notification text="This section is for <strong>Process Portal only</strong>. For <strong>Workplace</strong>, return to the <a href='#workplace'>top of section 2</a>."></inline-notification>

| **2.1** | **Task management and execution** |
| :--- | :--- |
| **Narration** | The customer service agent uses the Process Portal to work on their tasks. It is also used to launch processes and view the process dashboards. |
| **Action** &nbsp; 2.1.1 | Show the **Process Portal** that you opened during your preparation. Navigator's Work Dashboard may also be used but note the capabilities are different and the default narration does not match. <br/> <img src="./images/four.png" width="800" /><br/> |
| **Narration** | We are looking at the task list for the customer service agent. <br/> <br/> Process Portal is highly customizable to fit your organization's look and feel. The responsive user interface provides flexibility to get work done anywhere, at any time, on any device type, from a desktop device in the office to a mobile device at home or at a customer site. It can be configured through a set of options without having to customize the Process Portal application itself. <br/> <br/> Process Portal has a robust search capability. You can create a customized task list, for example, with specific business data, by saving task-based searches for later use. <br/> <br/> Customer service agents use the task list to organize and work on the tasks assigned to them. Our agent received a new investigation task. |
| **Action** &nbsp; 2.1.2 | Click any **Refund Investigation Issue** task. <br/> <img src="./images/Step_2.1_SaaS_action_2.png" width="800" /><br/> |
| **Narration** | Once I open the task, I will have all the information needed to investigate the refund. Now, I'll claim the task. |
| **Action** &nbsp; 2.1.3 | Click **Claim Task**. <br/> <img src="./images/Step_2.1_SaaS_action_3.png" width="800" /><br/> |
| **Narration** | Let’s review the request data and make an approval decision. |
| **Action** &nbsp; 2.1.4 | Click **Approve Refund**. <br/> <img src="./images/Step_2.1_SaaS_action_4.png" width="800" /><br/> |
| **Narration** | Behind the scenes, the refund process is managed by workflow. Once the investigation task is completed, the system automatically updates Focus Corp’s ordering application and notifies the customer. <br/> <br/> Although the process is managed by workflow, there is currently no straight-through processing since every request must be examined by a customer service agent. Let’s go back to the process diagram and see how we can improve things with straight-through processing. |

<br/>

</details>

**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>3 - Changing the workflow for straight-through processing</summary><br/>

| **3.1** | **Introduce straight-through processing automation** |
| :--- | :--- |
| **Narration** | Let’s look at how we can streamline the refund process by combining workflow and decision management. |
| **Action** &nbsp; 3.1.1 | Go back to the **Process Designer** tab, and click **Processes** in the menu on the left side. Click **Request Refund**. <br/> <img src="./images/Step_3.1_action_2.png" width="800" /><br/> |
| **Action** &nbsp; 3.1.2 | You will see the following process diagram. <br/> <img src="./images/Step_3.1_final_screen.png" width="800" /><br/> |
| **Narration** | We’ve added a decision task to the workflow that will automatically look at each request and make a refund decision without human intervention. This means that most requests can now be approved or declined in real time. Those that can’t are still routed for manual investigation. <br/><br/> Therefore, we can achieve a significant amount of straight-through processing where we completely process refund requests without human intervention. |


**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>4 - Executing the workflow with straight-through processing</summary><br/>

| **4.1** | **Refund request approved** |
| :--- | :--- |
| **Narration** | Let’s look at how straight-through processing transforms the refund process. |
| **Action** &nbsp; 4.1.1 | Go to Focus Corp's **Your Returns and Refunds** page. <br/> <img src="./images/Stu_7.2.png" width="800" /><br/> |
| **Action** &nbsp; 4.1.2 | Select the order ending in **AP**. <br/> <img src="./images/Step_4.1_action_2.png" width="800" /><br/> |
| **Action** &nbsp; 4.1.3 | Click **Submit Request** to process the refund. <br/> <img src="./images/Step_4.1_action_3.png" width="800" /><br/> |
| **Action** &nbsp; 4.1.4 | The process executes and generates a **Refund Approved** result.<br/><br/> <img src="./images/Step_4.1_results_screen.png" width="800" /><br/> |
| **Narration** | In this first example, when the customer submits the refund request, the criteria are evaluated by business rules and approval is granted in real time, avoiding a time-consuming manual investigation. |

| **4.2** | **Refund request denied** |
| :--- | :--- |
| **Narration** | Let’s look at a second example. |
| **Action** &nbsp; 4.2.1 | Click **Submit the next request**. <br/> <img src="./images/Script4.2.1.png" width="800" /><br/> |
| **Action** &nbsp; 4.2.2 | Select the order ending in **DE**. <br/> <img src="./images/Step_4.2_action_2.png" width="800" /><br/> |
| **Action** &nbsp; 4.2.3 | Click **Submit Request** to process the refund. <br/> <img src="./images/Step_4.2_action_3.png" width="800" /><br/> |
| **Action** &nbsp; 4.2.4 | The process executes and generates a **Refund Denied** result. <br/> <img src="./images/Step_4.2_results_screen.png" width="800" /><br/> |
| **Narration** | This request clearly did not meet Focus Corp's criteria and resulted in a denial because it was well outside the time window. Even though this refund request resulted in a denial, it was still straight-through processing because there is no manual work. |

| **4.3** | **Refund request requires manual investigation** |
| :--- | :--- |
| **Narration** | But what if the business rules determine a request requires investigation?  |
| **Action** &nbsp; 4.3.1 | Click **Submit Another Refund Request**. <br/><br/><img src="./images/Step_4.3_action_1.png" width="800" /><br/> |
| **Action** &nbsp; 4.3.2 | Select the order ending in **MA**.<br/><br/><img src="./images/Step_4.3_action_2.png" width="800" /><br/> |
| **Action** &nbsp; 4.3.3 | Click **Submit Request** to process the refund. <br/><br/><img src="./images/Step_4.3_action_3.png" width="800" /><br/> |
| **Action** &nbsp; 4.3.4 | The process executes and generates a **Refund Investigation** result.<br/><br/><img src="./images/Step_4.3_results_screen.png" width="800" /><br/> |
| **Narration** | In this case, workflow routes the request to a customer service agent to do the investigation. |

<br/>

**[Go to top](#top)**

</details>

<span id="spanID"></span>
<details markdown="1">

<summary>5 - Monitoring operational intelligence</summary><br/>

| **5.1** | **Review the refund dashboard** |
| :--- | :--- |
| **Narration** | Let’s look at the refund dashboard to see how much straight-through processing we’ve achieved. |
| **Action** &nbsp; 5.1.1 | Click the **Refund Dashboard** tab that you opened during your preparation. In this step, you are just speaking to the displayed dashboard. <br/> <img src="./images/Step_5.1_action_1.png" width="800" /> |
| **Narration** | So far, the percentage of manually processed requests is still around 70%, with the average manual investigation taking over two hours. <br/> <br/> Let’s look at what’s behind this dashboard. <br/> <br/> First, as the refund process runs, the system can collect and process historical data and make it available for visualization. <br/> <br/> Next, the Business Performance Center is a no-code monitoring application in the IBM Cloud Pak for Business Automation. Dashboards can be designed and shared in minutes that provide insight into important business activities and processes. You can prepare, design, and track visualizations of metrics, key performance indicators (KPIs), and other measurements of business performance in customizable dashboards. <br/> <br/> Additionally, the historical data can be used to feed a data lake to apply machine learning to your automations. For example, to make even more sophisticated refund decisions, we could use a data lake to incorporate machine learning into our refund process. The Cloud Pak for Business Automation includes some machine learning samples to help you get started. |

**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>6 - Modeling decisions</summary><br/>

| **6.1** | **Review the refund approval decision model** |
| :--- | :--- |
| **Narration** | Let’s look at how the business analyst can create and manage business rules to further increase straight-through processing. The business rules replicate how experts make refund decisions. <br/> <br/> Using no-code decision modeling, business analysts can easily author and test refund decision criteria. |
| **Action** &nbsp; 6.1.1 | Go to your **Decision Center** tab that you opened during your preparation. <br/> <img src="./images/DecisionCenter.png" width="800" /><br/> |
| **Action** &nbsp; 6.1.2 | Click the decision service named **Refund Processing**. <br/> <img src="./images/Step_6.1_action_2.png" width="800" /><br/> |
| **Action** &nbsp; 6.1.3 | When the **Refund Processing** decision screen appears, click **main**. <br/> <img src="./images/Step_6.1_action_3.png" width="800" /><br/> |
| **Action** &nbsp; 6.1.4 | The next screen has several blue tabs at the top. Make sure **Decision Model** is selected. <br/> <img src="./images/Step_6.1_action_4.png" width="800" /><br/> |
| **Narration** | This is the decision model for the refund request decision service. A decision model uses a diagram to break the decision (the top blue box) down into sub-decisions (additional blue boxes) and input data (green ovals), which all contribute to the final refund decision. |

| **6.2** | **Review the decision tables** |
| :--- | :--- |
| **Narration** | To partially automate the refund request process, we’ve used two main decision tables. A decision table groups rules with similar conditions and actions but use different thresholds or values. |
| **Action** &nbsp; 6.2.1 | Click **Validate Time Window** in the decision diagram. <br/> <img src="./images/Step_6.1_action_5.png" width="800" /><br/> |
| **Action** &nbsp; 6.2.2 | Click **Validate Time Window** in the **Decision logic** section on the left side of the screen, scrolling down as needed.  <br/> <img src="./images/Step_6.1_action_6.png" width="800" /><br/> |
| **Narration** | The first decision table considers the customer’s reason for return, the days since order, and the condition of the item. These are the same criteria that a customer service agent would use to make a refund request decision, but now the decision is automated and executes in real time. |
| **Action** &nbsp; 6.2.3 | Close the **Validate Time Window** table. <br/> <img src="./images/Step_6.1_action_7.png" width="800" /><br/> |
| **Action** &nbsp; 6.2.4 | Click **Validate Type of Goods** in the decision diagram. <br/> <img src="./images/Step_6.1_action_8.png" width="800" /><br/> |
| **Action** &nbsp; 6.2.5 | Click **Validate Type of Goods** in the **Decision logic** section on the left side of the screen, scrolling down as needed. <br/> <img src="./images/Step_6.1_action_9.png" width="800" /><br/> |
| **Narration** | The second sub-decision has a table that considers the type of item being returned together with its condition. |
| **Action** &nbsp; 6.2.6 | Close the **Validate Type of Goods** table. <br/> <img src="./images/Step_6.1_action_10.png" width="800" /> <br/>|

| **6.3** | **Make the final refund decision** |
| :--- | :--- |
| **Narration** | The final refund decision is made by combining the results of the 'Validate Time Window' and 'Validate Type of Goods' sub-decisions. |
| **Action** &nbsp; 6.3.1 | Click **Final Refund Decision** in the decision diagram. <br/> <img src="./images/Step_6.1_action_11.png" width="800" /><br/> |
| **Action** &nbsp; 6.3.2 | Click **Manual Decision** in the **Decision logic** section on the left side of the screen, scrolling down as needed. <br/> <img src="./images/Step_6.1_action_12.png" width="800" /><br/> |
| **Narration** | We’ve combined the two sub-decisions to make the final response using a simple text rule. <br/><br/> Business analysts can change the rules to achieve higher levels of straight-through processing or to adapt to changing business conditions. |
| **Action** &nbsp; 6.3.3 | Close the **Manual Decision** text rule. <br/> <img src="./images/Step_6.1_action_13.png" width="800" /><br/> |

**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>7 - Improving and testing the decisions</summary><br/>

| **7.1** | **Compare two versions of the refund decision model** |
| :---         | :--- |
| **Narration** | After running these rules for a few weeks, we realize we can further reduce manual investigations without increasing our risk. <br/> <br/> The decision model can be changed without having to change the underlying process application. <br/> <br/> The business analyst previously created a new version of the decision model to enhance the level of straight-through processing by reducing the number of manual investigations. <br/> <br/> Now, let’s compare the before and after versions to see what changed. |
| **Action** &nbsp; 7.1.1 | On the top left of the Decision Center, click the arrow next to **main** and select **Reduce Manual Processing**. <br/> <img src="./images/Step_7.1_action_1.png" width="800" /><br/> |
| **Action** &nbsp; 7.1.2 | Click the **maximize** icon towards the top right of the Decision Center (right below the blue bar). This opens the Decision Model view. <br/> <img src="./images/Step_7.1_action_2.png" width="800" /><br/> |
| **Action** &nbsp; 7.1.3 | Click the **Compare** icon on the top right of the Decision Model view. <br/> <img src="./images/Step_7.1_action_3.png" width="800" /><br/> |
| **Action** &nbsp; 7.1.4 | When a window opens to prompt a comparison of V1.0 and the current version, click the **Compare** button. <br/> <img src="./images/Step_7.1_action_4.png" width="800" /><br/> |
| **Action** &nbsp; 7.1.5 | Click the arrows next to the two changes on the top left to display rule changes above the two decision diagrams. <br/> <img src="./images/Step_7.1_action_5.png" width="800" /><br/> The comparison details will appear. <br/> <img src="./images/Step_7.1_action_5b.png" width="800" /><br/> |
| **Narration** | We select the two versions we wish to compare and see a side-by-side comparison of the two versions with details of the changes highlighted in the diagram and summarized above. &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
| **Action** &nbsp; 7.1.6 | To prepare for the next section, click **Reduce Manual Processing** at the top left side of the page. <br/> <img src="./images/Step_7.1_action_6.png" width="800" /><br/> |

| **7.2** | **Test a new version of the refund decision model** |
| :---         | :--- |
| **Narration** | The business analyst can also validate that the updated rules pass the regression test suite. One or more test suites can be created and executed. Let’s run one now and review the results. |
| **Action** &nbsp; 7.2.1 | Click the **Tests** tab. <br/> <img src="./images/Step_7.1_action_7.png" width="800" /><br/> |
| **Action** &nbsp; 7.2.2 | Click the **run** icon next to **Refund Process Operation**.  <br/><br/><inline-notification text="Make sure you are on the <strong>Test Suites</strong> sub-tab and not on the <strong>Reports</strong> sub-tab."></inline-notification> <br/> <img src="./images/Step_7.1_action_8.png" width="800" /><br/> |
| **Action** &nbsp; 7.2.3 | Click **OK** on the **Run Test Suite** dialog box. <br/> <img src="./images/Step_7.1_action_9.png" width="800" /><br/> |
| **Action** &nbsp; 7.2.4 | Click the name of your report to access it. <br/> <img src="./images/Step_7.1_action_10.png" width="800" /><br/> |
| **Action** &nbsp; 7.2.5 | You will see the following test suite report. <br/> <img src="./images/Step_7.1_final_comparison_report.png" width="800" /><br/> |
| **Narration** | All the scenarios succeeded, and the results were all as expected. <br/><br/>Once ready, the new version of the rules can be pushed into production by the business team (if they have the permission) or the IT team, depending on your governance processes. |

**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>Summary</summary>

Using the Cloud Pak for Business Automation, we had all the capabilities needed to significantly reduce the amount of manual refund processing. We combined workflow and decision automation to increase straight-through processing, which resulted in a lower average completion time, lower costs, and more consistent customer communication throughout the process.

Thank you for attending today’s presentation.

**[Go to top](#top)**

</details>
