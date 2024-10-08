---
title: Tasks
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/style-guide/style/tasks/
---

# Tasks

A *task* is an action that users perform to achieve a goal, such as creating a server. A task topic, article, or section provides the action steps and the necessary context and reference information that the user needs to complete the task.

This topic provides guidelines for developing tasks.

## Task Titles

The title of a task topic, article, or section begins with the imperative form of the task action, and it uniquely, precisely, and clearly describes the task. Use a plural subject unless the singular makes more sense or is necessary for clarity.

- Restart a Running Deployment

- Install Ops Manager from Archive on Linux

- Add Existing MongoDB Processes to Ops Manager

To learn how to capitalize titles, see Titles and Headings.

## Task Page Structure

### Task Introductions

Before providing steps, set the context for the task as necessary. For example, you could state the reason for completing the task, the method to be used, and the expected result. You might also state the intended audience and suggest the amount of time that the task might take, especially if it will take a long time.

- If the article or section title provides sufficient context, you can omit an introduction.

- Avoid providing extensive overview or conceptual text in the introduction to a task. Provide that information in a separate informational topic or in a topic that introduces the task as part of a larger process or user goal.

### Considerations

If the task has items that the user should acknowledge or contemplate before taking action, describe them in a "Considerations" section that precedes any prerequisites or the procedure. You could include the following information:

- Descriptions of variations, options, or scopes

- Hyperlinks to information that prepares the user for any choices they must make

- Impacts on other areas of the product or later tasks they might want to complete

### Prerequisites

If the task has requirements that the user *must* meet *before* taking action, describe them in a "Prerequisites" section that precedes the steps. You could include the following information:

- A hyperlink to a preceding task, if that task must be performed before this task

- Software that must already be installed, accessible, or running

- Access rights that are required for users to perform the task

- Hyperlinks to other topics that contain requirements or prerequisite tasks that the user must perform

Avoid including detailed procedures in a prerequisites section. Provide prerequisite tasks in other articles or sections, which you can reference in this section.

### Procedures

A task contains one or more *procedures* or sets of sequential action steps. Consider the following guidelines when creating a procedure:

- If the procedure has more than one step, use the `.. procedure::` directive for the steps. Don't use bullets, except to list choices within a step.

- If the procedure has more than one step, follow the guidance for introducing lists to introduce the procedure. To learn more, see Lists.

- If a procedure has nested steps, use ordered lists within the `.. step::` directive. The first level of nesting should use `a, b, c`, and so on. The next level of nesting should use `i, ii, iii`, and so on. Don't nest any more than that. To learn more, see Lists.

- If the procedure has only one step, show that step in a regular paragraph. That is, don't number it.

- If you have lengthy introductory or prerequisite information, or if you have more than one procedure, provide a heading for the procedure or procedures. Use the imperative form of the action and a singular form of the object. Don't repeat the title of the task article.

- Try to limit procedures to 10 steps. If you have more than 10 steps, consider whether you can divide the steps into two or more procedures. Creating several short, simple, and sequential procedures instead on one long, complex procedure, especially one with many substeps and choice steps, will help users know where they are in the process, judge their progress, and complete the task successfully.

### Steps

When writing steps, use the following guidelines.

#### Use Imperative Sentences

Write each step as a complete and correctly punctuated imperative sentence (that is, a sentence that starts with an imperative verb). In steps, the focus is on the user, and the voice is active.

1. Log in to the Cloud Control Panel.

2. Use the following command to start `vsftpd`:

   ```sh
   sudo service vsftpd start
   ```

#### Show One Action Per Step

Usually, include only a single action in each step. If two actions are closely related, such as opening a menu and selecting a command from the menu, you can include both actions in one step.

1. Under **Export**, select your database (for example, 388488_drupal).

2. Scroll down to the bottom of the window and select the **Save as file** check box, which will save your database output to a file.

3. Click **Go**.

4. If you're prompted to save your file, save it to your computer.

#### Provide Context Before the Action

If a step specifies where to perform an action, state where to perform the action before describing the action.

1. In the navigation pane, click **Inbound Rules**.

2. On the Binding and SSL Settings page, perform the following steps:

#### Provide Conditions Before the Action

If a step specifies a situation or a condition, state the situation or condition before describing the action.

1. If a new version is available, click **Install**.

2. To find out the encryption type of your Windows computer (32-bit or 64-bit), navigate to the server's Control Panel and click **System**.

#### Follow the Step with Explanatory Information

Don't include explanatory or reference information in the action part of a step. If needed, follow the step with one or more paragraphs that provide supplemental information.

1. In the **Body Match** text box, enter a word or phrase that will appear on the page when it loads successfully.

   For example, you can perform a body match on the copyright date to verify whether the website is running.

#### Show Only Actions as Steps

Don't show system actions, responses, or results as steps. Put necessary statements in unnumbered paragraphs following the steps to which they apply. See the first example in the "Examples" section.

When the result of a step is the appearance of a dialog box, window, or page in which the action of the next steps occurs, you can usually eliminate a result statement and orient the user at the beginning of the next step. See the second example in the "Examples" section.

*Use:*

1. On Linux, enter the following command:

   ```sh
   sudo MongoDB-monitoring-agent --setup
   ```

   The list of setup settings is displayed.

*Use:*

1. Under **Other Options** in the MongoDB Email box, select **Mobile Sync**.

2. On the Activate Mobile Sync page, select individual users to activate, or select the **Add Mobile Sync to all mailboxes on this domain** option.

#### Use Screenshots Sparingly

Screenshots can help to orient the user, but a screenshot of every field or dialog box usually isn't necessary.

If you include screenshots, place each one directly under the step that it illustrates. Don't rely on the screenshot to show information or values that the user must enter; always provide that information in the text of the steps. However, ensure that the screenshot accurately reflects the directions and values in the step text.

To learn more about when to use screenshots, see Screenshot Guidelines and Process.

#### Label Optional Steps

To indicate that a step is optional, include *(Optional)*, in italics, as a qualifier at the beginning of the step.

1. *(Optional)* Click **Advanced Options**.

#### Omit Extraneous Words

Omit extraneous words (such as *pop-up menu* or *command button*) unless they're needed for clarity.

*Use:*

1. In the Disks window, right-click the volume and select **Take Offline**.

*Avoid:*

1. In the Disks window, right-click the volume and select **Take Offline** from the pop-up menu.

*Use:*

1. Click **Add**, enter a name for the profile, and then click **OK**.

*Avoid:*

1. Click the **Add** button, enter a name for the profile in the text box, and then click the **OK** button.

#### Show Multiple Possibilities in a List

If a step directs the user to choose from multiple possibilities, use an unordered list to present the possibilities.

1. Select a volume type:

   - **Standard**: A standard SATA drive for users who need additional storage on their server

   - **High Performance**: An SSD drive, which offers a higher performance option for databases and high performance applications

#### Document only One Method

If more than one method exists for completing an action, document only one method, usually the most efficient or preferred method.

*Use:*

1. Select **File > New**.

*Don't use:*

1. Select **File > New**, or press **Ctrl+N**.

## Results, Verification, Examples, and Troubleshooting

Following the procedure or procedures, include the following information if it's necessary or helpful to the user. If the information is brief, you can include it directly following the last step in the procedure. If it's lengthy or you need to provide more than one type of information, use sections with headings.

- The result of performing the task.

- Information about verifying successful completion of the task, such as the location of logs. If verification is a separate task in a different article or section, provide a hyperlink to it under a "Where to go from here" heading.

- An example that illustrates or supports the task.

- Information about what to do if the procedure doesn't work. This information might be a hyperlink to a separate troubleshooting topic.

## Direction to the Next Action

If your task is part of a larger set of tasks, you can help the user by including a "Where to go from here" section. You might include the following information:

- A brief explanation of the next task and why the user needs to perform it, accompanied by a hyperlink to the next task.

- Hyperlinks to other tasks that could be done next, if multiple options are available. Describe the multiple options so that users know which task to choose.

## Related Topics

To provide a quick way for the user to access other content that's related to the task, provide links to the content at the end of the article or topic. Even if you have already included an embedded hyperlink to the material in the article or topic, you can provide the hyperlink again under "Related topics," but typically you should provide a link only once in an article or section. For more information about linking, see Links and Cross-References.