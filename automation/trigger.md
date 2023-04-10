---
description: The event that triggers the automation to start.
---

# Trigger

In Logic Sheet, you can set up triggers to initiate automation workflows based on specific events or times. There are three types of triggers to choose from: Time driven, On edit, On form submission, and on webhook calls.

### Choose a trigger type

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

**On edit triggers** include "Spreadsheet is edited", "A new row is inserted", and "A new column is inserted".&#x20;

**The form submission trigger** will run when your spreadsheet has received a form submission. This trigger will only work when you have connected a Google Form with a spreadsheet.&#x20;

**A webhook response is received:** Run when the spreadsheet has received a webhook response. To use this trigger, you need to set up a [webhook](add-connections/webhook.md).

{% hint style="warning" %}
Currently, you can only set up one automation with each one of the above-mentioned three types of triggers. For example, if you have created a "Spreadsheet is edited" trigger, which is a type of "On edit trigger" in one spreadsheet, you cannot create another on edit trigger, such as "A new row is inserted," in the same spreadsheet.

A possible solution to this limit is our [Conditional action](actions/conditional-actions.md) feature.&#x20;
{% endhint %}

{% hint style="info" %}
Please refer to the above hint box if you see the following error message:

_`An error happened. Error message: Exception: This add-on has created too many time-based triggers in this document for this Google user account.`_
{% endhint %}

### Sheet

In the trigger step, you will be asked to choose a sheet (or worksheet) for the automation.&#x20;

In most cases, this option will affect how the [conditions](conditions.md) you set to run the automation. For example, in the [conditions step](conditions.md), if you choose a range condition and set the range as "A1," the app will look up the A1 range in the worksheet you have chosen in the trigger step.

{% hint style="info" %}
If your trigger type is "A form response is received," you have to set the sheet here as the worksheet that is receiving form responses.
{% endhint %}
