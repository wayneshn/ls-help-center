# Send an email

This action will send an email from your Gmail account.

![Email sent by Logic Sheet](<../../.gitbook/assets/image (62).png>)

### To (required)

The recipient(s) of the email. It should be the email address or email addresses that will receive this email. You can set up multiple email addresses separated by a comma in this field.

**Multiple fixed emails**

```
email1@example.com, mail2@example.com
```

**Multiple emails using merge tag**

Suppose that the value in cell B5 and F4 are email addresses, you can do this for the recipients:

```
email@example.com, {{range B5}}

OR

{{range B5}}, {{range F4}}
```

### Subject (required)

The subject of the email.

### Email body (required)

The email content.

{% hint style="success" %}

#### Merge tag available

You can use the following merge tags in the Value field here. See [how merge tags work](../merge-tags.md).

-   \{{range A1\}}: The value of cell A1(dynamic), or other cells of your choice.
-   \{{old value\}}: The value of the cell prior to editing.
-   \{{new value\}}: The new value of the cell after being edited.
-   \{{editor\}}: The email address of the user who made the edit.
-   \{{edited range\}}: The notation (string) of the cell being edited.
-   \{{column A\}}: All values in column A(dynamic).
-   \{{row 1\}}: All values in row 1(dynamic).
-   \{{sheet\}}: The name of the sheet that was edited or set in the trigger step.
-   \{{spreadsheet url\}}: The URL of the spreadsheet that this automation belongs to.
-   \{{automation name\}}: The name of the automation workflow you have set.
-   \{{form values\}}: All values of the form submission that was received.
-   \{{form values 1\}}: The first value (or the nth value if you set the number as n) of the form submission that was received.

{% endhint %}

### Optional fields

You can optionally fill in these fields.

-   Sender name: The name that will be shown in the receiver's inbox as the sender name.
-   CC: A list of email addresses that this email will copy to.
-   BCC: A list of email addresses that this email will blind carbon copy to.
-   Reply to: An email address to use as the default reply-to address (default: the user's email address).
