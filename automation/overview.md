---
description: >-
  Logic Sheet Automation lets you automate your spreadsheets with action rules,
  which allow you to send notifications when editing or form submissions occurs
  or at designated times.
---

# Automation overview

Use Logic Sheet Automation to streamline your Google Sheets tasks.&#x20;

With Logic Sheet, you can set up triggers that initiate specific actions upon certain events, such as when a cell is edited or a form is submitted, or at a predetermined time.&#x20;

To create an automation workflow in Logic Sheet, you will need to establish a trigger, optional conditions, and at least one action.&#x20;

All of your automations for a single document can be accessed from the Automation tab in the Logic Sheet sidebar.

You can view and manage all of your automations from the Automation tab in the Logic Sheet sidebar.&#x20;

To turn an automation on or off, click the toggle bar next to the automation.&#x20;

To delete an automation, click the Kebab menu and select "Delete." Confirm the deletion in the pop-up prompt, and the automation will be removed.&#x20;

To add a new automation, click the "New automation" button and use the automation builder to set up the trigger, conditions, and actions. It is good practice to change the name of your automation workflow as soon as you open the automation builder.

![Logic Sheet Automation Builder](<../.gitbook/assets/image (21).png>)

To make an automation workflow, you need to go through [Trigger](trigger.md), [Conditions](conditions.md), and [Actions](actions/).

### [Trigger](trigger.md)

A trigger is the event that initiates the automation workflow. In Logic Sheet, you can set up the following triggers:

* On edit: This trigger will run the automation workflow whenever the specified cells are edited.
* On form submission: This trigger will run the automation workflow whenever a form linked to the spreadsheet is submitted.
* At a specific time of day: This trigger will run the automation workflow at a specific time each day, week, or month.
* A webhook response is received: Run when the spreadsheet has received a webhook response. To use this trigger, you need to set up a [webhook](add-connections/webhook.md).
* See more trigger options on the [Trigger](trigger.md) page.

### [Conditions (optional)](conditions.md)

Conditions allow you to specify additional criteria that must be met in order for the automation workflow to run. For example, you can set up a condition to only run the automation if the value of a specific cell meets a certain criterion.

### [Actions](actions/)

An action is the task that will be performed when the automation workflow is triggered. In Logic Sheet, you can set up the following actions:

* Send an email: This action will send an email with specified content and recipients.
* Update cell value: This action will update the value of a specific cell in the spreadsheet.
* Create a new row: This action will add a new row to the spreadsheet with specified values.
* See more action on the [Actions](actions/) page.
