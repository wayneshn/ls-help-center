---
description: >-
  Merge tags enable you to reference to dynamic data in your spreadsheet or the
  context data of the automated workflow you are building.
---

# Merge tags

Merge tags are used to refer to dynamic data in Logic Sheet automation. When you use merge tags in fields that accept merge tags, the app will "translate" them into their corresponding values when the workflow is being executed. For example, if you use the merge tag \{{range B12\}} in an email, the merge tag will be replaced by the value in cell B12 when the email is sent.

### Format

Merge tags are all wrapped in double curly braces as in \{{merge tag\}}. While some merge tags are static, like \{{automation name\}} and \{{spreadsheet url\}}, others can be dynamic as you can change them to refer to more specific values, like \{{last row 3\}} and \{{last row 5 value\}}.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Each time you edit an input where merge tags are allowed, you will see a preview of the merge tags used as shown in the above screenshot. This feature allows you to preview what the merge tags will look like when the workflow is being executed.
{% endhint %}

### Dynamic merge tags

Merge tags like \{{range A1\}}, \{{column A\}}, and \{{form values 1\}} are dynamic. It means that you can change the values in the merge tags to refer to different data.

For example, in the merge tag \{{range A1\}}, you can change the value "A1" into "B10" to make the merge tag refer to the value in cell B10.

In \{{form values 1\}}, you can change the number 1 into 3 to make it \{{form values 3\}}, which will refer to the 3rd value of the form submission that was received.

### Trigger limits

Some merge tags only work with specific types of triggers. For example, the merge tags \{{old value\}} and \{{new value\}} only work with the trigger type "The spreadsheet is edited" because they only exist when there is an editing behavior.

Similarly, the merge tags \{{form values\}} and \{{form values 1\}} are only available in the "A form response is received" trigger, because these values cannot be found in other trigger types.

{% hint style="danger" %}
Please note that if you use a merge tag that is limited to one trigger type in a different trigger type, you may see an error message when setting up the automation.
{% endhint %}

<figure><img src="../.gitbook/assets/image (52).png" alt=""><figcaption><p>What happens when we try to use the {{edited range}} in a time-driven trigger</p></figcaption></figure>

### **How to use merge tags**

#### **\{{range A1\}}**

The value of the range A1 of the worksheet you have selected. You can change the range to refer to any other cell such as \{{range B10\}} and \{{range F9\}}. Since this merge tag only returns one value, multi-cell ranges will only return the value of the first range. For example, \{{range A2:B10\}} will return the value of range A2.

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption><p>How to use {{range A1}} merge tag in Logic Sheet</p></figcaption></figure>

{% hint style="warning" %}
Some inputs expect a range value, and if you use a merge tag that will return a value, you may encounter an error. For example, in the condition step, if you use a merge tag that represents a value in the input "When the value of cell" (which expects a cell range, you may see the following warning message.

In this case, you will need to change the merge tag to something that represents a cell range, like \{{last row 4\}}, \{{edited range\}}, use simply type a cell range without the merge tag, like A1, F5.
{% endhint %}

<figure><img src="../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>

#### **\{{column A\}}**

All values in column A(dynamic). You can use other values like \{{column B\}}, \{{column G\}} as well.

<figure><img src="../.gitbook/assets/image (53).png" alt=""><figcaption><p>Merge tag {{column C}} will return all values in column C. The values will be separated by commas.</p></figcaption></figure>

#### **\{{row 1\}}**

All values in row 1(dynamic). You can use other values like \{{row 3\}}, \{{row 99\}} as well.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption><p>Merge tag {{row 4}} will return all values in row 4. The values will be separated by commas.</p></figcaption></figure>

#### **\{{sheet\}}**

The name of the sheet that was edited or set in the trigger step.

<figure><img src="../.gitbook/assets/image (79).png" alt=""><figcaption><p>The merge tag {{sheet}} in this example returns the worksheet name "Product".</p></figcaption></figure>

#### **\{{automation name\}}**

The name of the automation workflow you have set.

<figure><img src="../.gitbook/assets/image (59).png" alt=""><figcaption><p>Automation name cannot be preview in the setup step. But nevertheless, it will return the name of the automation you have set.</p></figcaption></figure>

#### **\{{spreadsheet url\}}**

The URL of the spreadsheet that this automation belongs to.

<figure><img src="../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

#### **\{{last row 1\}}**

The **A1 notation** of the first cell at the 1st column of the last row. Accordingly, \{{last row 5\}} returns the **A1 notation** of the cell at the 5th column of the last row.

<figure><img src="../.gitbook/assets/image (64).png" alt=""><figcaption><p>The merge tag {{last row 2}} will return B10 in this example.</p></figcaption></figure>

{% hint style="info" %}
This merge tag only refers to the cell name, not the value in the cell. For the value in the cell, use the \{{last row 1 value\}} merge tag.&#x20;

In this example, \{{last row 3\}} will return "C3", whereas \{{last row 3 value\}} returns "Sam".

<img src="../.gitbook/assets/image (76).png" alt="" data-size="original">
{% endhint %}

#### &#x20;**\{{last row 1 value\}}**

The **value** of the first cell at the 1st column of the last row. Accordingly, \{{last row 5\}} returns the **value** of the cell at the 5th column of the last row.

<figure><img src="../.gitbook/assets/image (72).png" alt=""><figcaption><p>The merge tag {{last row 2 value}} will return "Product LUNZZ" in this example.</p></figcaption></figure>

{% hint style="success" %}
You can also use column names in the last row merge tags. For example, \{{last row C values\}} is equal to \{{last row 3 value\}}.
{% endhint %}

#### **\{{old value\}}**

<mark style="color:orange;">Available in the "A spreadsheet is edited" trigger only.</mark> This merge tag will return the old value of the cell that has been edited. If an empty cell was edited, this merge tag will return "undefined". For example, if cell A1 was edited from 10 to 100, this merge tag will return 10.

{% hint style="info" %}
This merge tag, like merge tags that are only available in the "A spreadsheet is edited" trigger, cannot be previewed because their data is only available when the automation is being executed. But you will see a green text telling you the merge tag is valid when previewing it.

![](<../.gitbook/assets/image (51).png>)
{% endhint %}

#### **\{{new value\}}**

<mark style="color:orange;">Available in the "A spreadsheet is edited" trigger only.</mark> This merge tag will return the new value of the cell that has been edited. For example, if cell A1 was edited from 10 to 100, this merge tag will return 100.

#### **\{{editor\}}**

<mark style="color:orange;">Available in the "A spreadsheet is edited" trigger only.</mark> This merge tag will return the email address of the user who edited the spreadsheet.

#### **\{{edited range\}}**

<mark style="color:orange;">Available in the "A spreadsheet is edited" trigger only.</mark> This merge tag will return the cell that has been edited in an on-edit trigger. For example, if cell A1 was edited from 10 to 100, this merge tag will return the text "A1".

#### **\{{form values\}}**

&#x20;<mark style="color:orange;">Available in the "A form response is received" trigger only.</mark> All values of the form submission that was received. Values are separated by commas.

#### **\{{form values 1\}}**

<mark style="color:orange;">Available in the "A spreadsheet is edited" trigger only.</mark> The first value (or the nth value if you set the number as n) of the form submission that was received.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

In the above example, we are using a Google Form to receive feature requests. When the automation is triggered, \{{form values 2\}} will return the second value of the form response, or the Feature name, and \{{form values 3\}} will return the Description of the feature requested.

#### **\{{triggering row N value\}}**

<mark style="color:orange;">Available in the "A spreadsheet is edited" trigger only.</mark> The merge tag will return the **value** of the cell at column N in the same row where the automation is triggered.&#x20;

#### **\{{triggering row N\}}**

<mark style="color:orange;">Available in the "A spreadsheet is edited" trigger only.</mark> The merge tag will return the **A1 notation** of the cell at column N in the same row where the automation is triggered.&#x20;

&#x20;In the following example, if the automation was triggered by an edit in range B3, \{{triggering row C value\}} will be the value of range C3, or 1396. \{{triggering row C\}} will return the range name of C3.

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>
