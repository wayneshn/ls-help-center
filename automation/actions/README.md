---
description: Actions to run when the automation is triggered.
---

# Actions

Once an automation is triggered and the conditions are met, Logic Sheet will run actions that you have set in this step.

{% hint style="warning" %}
You need at least one action to make a complete automation. If no action is set, the automation will not run.
{% endhint %}

### Add an action

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Click the "Add an action" button and configure the action. Currently, we support the following types of actions.

* [Send an email](send-an-email.md), which will send an email from your Gmail account.
* [Send a Slack message](send-a-slack-message.md), which will send a message to a specific channel in the Slack workspace you have authorized to.
* [Update Airtable](update-airtable.md), which updates a table in your Airtable account automatically.
* [Recalculate the current sheet](recalculate-the-current-sheet.md), which will hard refresh the worksheet you chose in the trigger step and refresh the results of formulas set in the worksheet.&#x20;
* [Make an HTTP request](make-http-request.md): Send an HTTP request automatically.

### Remove an action

Click the close sign on the top right of each action form to remove an action.

### Action run sequence

Actions will run sequentially if you choose multiple actions.
