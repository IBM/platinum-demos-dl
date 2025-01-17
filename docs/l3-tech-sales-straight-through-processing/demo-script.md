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

| **2.1** | **Task management and execution (Workplace)** |
| :--- | :--- |
| **Narration** | The customer service agent uses Workplace to work on their tasks. It is also used to launch processes and view the process dashboards. |
| **Action** &nbsp; 2.1.1 | Show the **Workplace** window that you opened during your preparation. <br/> <img src="./images/Stu_4.4.4_Self_install.png" width="800" /> |
| **Narration** | We are looking at the task list for the customer service agent. <br/> <br/> Workplace is highly customizable to fit your organization's look and feel. The responsive user interface provides flexibility to get work done anywhere, at any time, on any device type, from a desktop device in the office to a mobile device at home or at a customer site. It can be configured though a set of options without having to customize the Workplace application itself. <br/> <br/> Workplace has a robust search capability. You can create a customized task list, for example, with specific business data, by saving task-based searches for later use. <br/> <br/> Customer service agents use the task list to organize and work on the tasks assigned to them. Our agent received a new investigation task. |
| **Action** &nbsp; 2.1.2 | Click any **Refund Investigation Issue** task. If prompted, **Claim the task**. <br/> <img src="./images/Step_2.1_ROKS_action_3.png" width="800" /> |
| **Narration** | Once I open the task, I will have all the information needed to investigate the refund. |
| **Action** &nbsp; 2.1.3 | Click **Approve Refund**. <br/> <img src="./images/Step_2.1_ROKS_action_5.png" width="800" /> |
| **Narration** | Let’s review the request data and make an approval decision. Behind the scenes, the refund process is managed by workflow. Once the investigation task is completed, the system automatically updates Focus Corp’s ordering application and notifies the customer. <br/> <br/> Although the process is managed by workflow, there is currently no straight-through processing since every request must be examined by a customer service agent. Let’s go back to the process diagram and see how we can improve things with straight-through processing. |



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
| **Narration** | Let’s look at how the business analyst can create and manage business rules to further increase straight-through processing. The business rules replicate how experts make refund decisions. <br/> <br/> Using no-code decision modeling, business analysts can easily author and test refund decision criteria. This is the decision model for the refund request decision service. A decision model uses a diagram to break the decision (the top blue box) down into sub-decisions (additional blue boxes) and input data (green ovals), which all contribute to the final refund decision. |
| **Action** &nbsp; 6.1.1 | Go to your **Refund Processing** decision modelling tab that you opened during your preparation. <br/> <img src="./images/Script6.1.1.png" width="800" /><br/> |


| **6.2** | **Review the decision tables** |
| :--- | :--- |
| **Narration** | To partially automate the refund request processing, we’ve used two main decision tables. A decision table groups rules with similar conditions and actions but use different thresholds or values. |
| **Action** &nbsp; 6.2.1 | Click **Validate Time Window** in the decision diagram. <br/> <img src="./images/Script6.2.1.png" width="800" /><br/> |
| **Action** &nbsp; 6.2.2 | Click **Logic (A)**, then click **Validate Time Window (B)**.  <br/> <img src="./images/Script6.2.2.png" width="800" /><br/> |
| **Narration** | The first decision table considers the customer’s reason for return, the days since order, and the condition of the item. These are the same criteria that a customer service agent would use to make a refund decision, but now the decision is automated and executes in real time. |
| **Action** &nbsp; 6.2.3 | Click **Back to the diagram**. <br/> <img src="./images/Script6.2.3.png" width="800" /><br/> |
| **Action** &nbsp; 6.2.4 | Click **Validate Type of Goods (A)**, **Logic (B)**, then click **Validate Type of Goods (C)**. <br/> <img src="./images/Script6.2.4.png" width="800" /><br/> |
| **Narration** | The second sub-decision has a table that considers the type of item being returned, and its condition. |
| **Action** &nbsp; 6.2.5 | Click **Back to the diagram**. <br/> <img src="./images/Script6.2.5.png" width="800" /><br/> |

| **6.3** | **Make the final refund decision** |
| :--- | :--- |
| **Narration** | The final refund decision is made by combining the results of the 'Validate Time Window' and 'Validate Type of Goods' sub-decisions. |
| **Action** &nbsp; 6.3.1 | Click **Final Refund Decision** in the decision diagram **(A)**, then click **Logic (B)**. <br/> <img src="./images/Script6.3.1.png" width="800" /><br/> |
| **Action** &nbsp; 6.3.2 | Click **Manual Decision**. <br/> <img src="./images/Script6.3.2.png" width="800" /><br/> |
| **Narration** | We’ve combined the two sub-decisions to make the final response using a simple text rule. <br/><br/> Business analysts can change the rules to achieve higher levels of straight-through processing or to adapt to changing business conditions. |
| **Action** &nbsp; 6.3.3 | Click **Back to the diagram**. <br/> <img src="./images/Script6.3.3.png" width="800" /><br/> |

**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>7 - Improving and testing the decisions</summary><br/>

| **7.1** | **Test the existing business logic** |
| :---         | :--- |
| **Narration** | After running these rules for a few weeks, we realize we can further reduce manual investigations without increasing our risk. <br/> <br/> The decision model can be changed without having to change the other components used in the refund process.<br/>  |
| **Action** &nbsp; 7.1.1 | Click **Run**. <br/> <img src="./images/Script7.1.1.png" width="800" /><br/> |
| **Action** &nbsp; 7.1.2 | Select **Manual** from the **Test data** list **(A)** to load the test scenario, then click **Run (B)**. <br/> <img src="./images/Script7.1.2.png" width="800" /><br/> |
| **Action** &nbsp; 7.1.3 | Review the **Decision output**. <br/> <img src="./images/Script7.1.3.png" width="800" /><br/> |

| **7.2** | **Update the business logic** |
| :---         | :--- |
| **Narration** | It has been determined that refund requests will now be denied when **all of the following conditions** are met:<br/><br/> - the refund reason is “no longer needed”<br/> - the number of days since the order was delivered is greater than 7<br/> - the goods condition is “worn or damaged”<br/><br/> If all of these conditions are met, the refund will be denied.|
| **Action** &nbsp; 7.2.1 | Select the **Modeling** tab. <br/> <img src="./images/Script7.2.1.png" width="800" /><br/> |
| **Action** &nbsp; 7.2.2 | Click the **Validate Time Window** decision node **(A)**, click **Logic (B)**, then click **Validate Time Window (C)**.  <br/> <img src="./images/Script7.2.2.png" width="800" /><br/> |
| **Narration** | In this decision table, the rules are checked in sequence, starting at the top on row 1. If none of the rows match the data in the refund request, the “Otherwise” rule on row 8 will apply and the decision table will return “approved”.<br/><br/>Currently, cases in which the goods are worn, but no longer needed result in manual processing. A new rule will be inserted into the decision table to deny refunds where the goods are worn, no longer needed, and more than 7 days have passed since delivery. In cases where less than 7 days have passed, the existing rule will apply, resulting in manual processing.<br/>|
| **Action** &nbsp; 7.2.3 | Right-click on **3 (A)**, select **Insert row (B)**, then select **Below (C)**. <br/> <img src="./images/Script7.2.3.png" width="800" /><br/> |
| **Action** &nbsp; 7.2.4 | Enter **7** in the **days since order delivered** cell in the new row. <br/> <img src="./images/Script7.2.4.png" width="800" /><br/> |
| **Action** &nbsp; 7.2.5 | Right-click the **days since order delivered** cell in the new row **(A)**, select **Change operator (B)**, then select the **greater than symbol (C)**. <br/> <img src="./images/Script7.2.5.png" width="800" /><br/> |
| **Action** &nbsp; 7.2.6 | Double-click the **goods condition** cell in the new row **(A)**, click the **down-arrow (B)** select **worn or damaged (C)**. <br/> <img src="./images/Script7.2.6.png" width="800" /><br/> |
| **Action** &nbsp; 7.2.7 | Double-click the **time window decision** cell in the new row **(A)**, click the **down-arrow (B)**, select **denied (C)**. <br/> <img src="./images/Script7.2.7.png" width="800" /><br/> |
| **Action** &nbsp; 7.2.8 | Hover your mouse over the decision table’s left border **(A)**, the rules representing each row of the table are displayed **(B)**. <br/> <img src="./images/Script7.2.8.png" width="800" /><br/> |

| **7.3** | **Test the new business logic** |
| :---         | :--- |
| **Action** &nbsp; 7.3.1 | Click **Run**. <br/> <img src="./images/Script7.3.1.png" width="800" /><br/> |
| **Narration** | The Manual test case previously returned the result “Manual”. <br/><br/>Now that the logic has been changed, the result of this test will be "denied". The rules in the decision table are applied in sequence, so initially the rule on row 3 will set the result to be "manual", but this will be superseded by the new rule on row 4. None of the other rule in the decision table will match the conditions of the refund, so the result from row 4 will be final. <br/> |
| **Action** &nbsp; 7.3.2 | Select the **Manual** test data **(A)** (this previously produced the result “Manual”). Click **Run (B)**, then note the updated result **“Denied” (C)**. <br/> <img src="./images/Script7.3.2.png" width="800" /><br/> |
| **Action** &nbsp; 7.3.3 | Modify the **daysSinceOrderDelivered** value, enter **6 (A)**, then click **Run (B)**. Note the updated result **“Manual” (C)**. <br/> <img src="./images/Script7.3.3.png" width="800" /><br/> |
| **Narration** | By changing the value of days since delivered attribute in the test data, the new rule won't match the refund, and the old rule will be the only rule to match.<br/><br/> Now that the business logic has been updated, a new version of the decision service could be deployed into production. Systems that consume the decision service would benefit immediately, automatically, and without an interruption to the service.   <br/> |

**[Go to top](#top)**

</details>
<span id="spanID"></span>
<details markdown="1">

<summary>Summary</summary>

Using the Cloud Pak for Business Automation, we had all the capabilities needed to significantly reduce the amount of manual refund processing. We combined workflow and decision automation to increase straight-through processing, which resulted in a lower average completion time, lower costs, and more consistent customer communication throughout the process.

Thank you for attending today’s presentation.

**[Go to top](#top)**

</details>
