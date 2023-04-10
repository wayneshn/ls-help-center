---
description: >-
  This feature allows you to add conditions to each of the actions you set, so
  that the actions will only run when the conditions are met.
---

# Conditional actions

Introducing Conditional Actions - the feature that gives you the power to add conditions to each of your actions, ensuring that they only run when specific conditions are met. This means you can easily set up multiple triggers with the same trigger type in the same spreadsheet, and run different actions based on different conditions. To get started, simply add a set of conditions to each action you have set.&#x20;

{% hint style="success" %}
Conditions are optional. If you don't set any conditions in action, the action will always run.
{% endhint %}

In each action, you can choose to add a set of conditions.&#x20;

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Heads up (if you used Logic Sheet before January 2023)!** We have improved the condition form. Now, you can compare two values directly instead of comparing the cell value to a specific value as before. To check if the value in cell A3 is equal to 10, simply enter \{{Range A3\}} in the first input and 10 in the "This value" input. In the edit trigger, to check if the edited range meets certain conditions, use the \{{New value\}} merge tag instead of the \{{edited range\}} tag.
{% endhint %}

You can choose multiple action conditions. If you do so, remember to choose whether you want the action to run when "all" of the conditions are met or when "any" of the conditions are met.

{% hint style="info" %}
This feature is useful when you want to set up multiple triggers with the same trigger type in the same spreadsheet. Remember, you cannot set up more than one same trigger type in one spreadsheet. With this feature, you can set up one trigger and run different actions based on different conditions.
{% endhint %}
