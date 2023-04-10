---
description: When should the automation be executed
---

# Conditions

This is an optional step that lets you set up a set of conditions when the automation is executed. You can use these properties to customize your rule as it is applied to your data, like when range A1 is equal to x.

<figure><img src="../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

Once you have clicked the "Add a condition button," you will see an option that lets you choose "When all/any of the conditions are/is met." If you choose "all," the automation will only run if all of the conditions you have set are met. If you choose "any," the automation will run if any of the conditions you have set are met.

#### When this value

In this field, you can type in the value that you want to compare. Usually, you will need to use a [merge tag](merge-tags.md) to refer to the dynamic data in your spreadsheet or in the context of an automation run. For example, \{{Range A1\}} will give you the value of cell A1. If you are using an edit trigger, \{{new value\}} will give you the new value when a cell is edited.

#### Condition

The Condition dropdown menu here refers to the operator of the comparison you want to make. Here are all the operators you can choose:

* is equal to
* is not equal to
* is greater than
* is greater than or equal to
* is less than
* is less than or equal to
* contains
* does not contain
* is empty
* is not empty

#### Value

The value to compare to. The following configuration will let the automation run only when cell A1 is greater than 100.

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
#### Merge tag available

You can use the following merge tags in the Value field here. See [how merge tags work](merge-tags.md).

* \{{range A1\}}: The value of cell A1, or other cells of your choice.
* \{{old value\}}: The value of the cell prior to editing.
* \{{new value\}}: The new value of the cell after being edited.
* \{{editor\}}: The email address of the user who made the edit.
* \{{edited range\}}: The notation (string) of the cell being edited.
{% endhint %}

{% hint style="success" %}
You can add or remove conditions by clicking on the "Add a condition" button or the close sign of each condition.
{% endhint %}

{% hint style="warning" %}
**Heads up (if you used Logic Sheet before January 2023)!** We have improved the condition form. Now, you can compare two values directly instead of comparing the cell value to a specific value as before. To check if the value in cell A3 is equal to 10, simply enter \{{Range A3\}} in the first input and 10 in the "This value" input. In the edit trigger, to check if the edited range meets certain conditions, use the \{{New value\}} merge tag instead of the \{{edited range\}} tag.
{% endhint %}
