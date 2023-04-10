# Send a Slack message

This action will send a Slack message using the Logic Sheet Slack bot.

![An example of how Logic Sheet Slack bot works](<../../.gitbook/assets/image (90).png>)

{% hint style="warning" %}
#### Authorization needed

You need to authorize your Slack Workspace to make this action work. If you haven't connected to a Slack Workspace, the "Send a Slack message" option will be disabled.

![](<../../.gitbook/assets/image (92).png>)

To connect to third-party services, click the "Add connection" button to open the service connector. [Read more about adding connections here](../add-connections/).
{% endhint %}

### Channel

The Slack channel to send the message to.

### Message

The message that will be sent to the channel selected. Plain text only.

{% hint style="success" %}
#### Merge tag available

You can use the following merge tags in the Value field here. See [how merge tags work](../merge-tags.md).

* \{{range A1\}}: The value of cell A1(dynamic), or other cells of your choice.
* \{{old value\}}: The value of the cell prior to editing.
* \{{new value\}}: The new value of the cell after being edited.
* \{{editor\}}: The email address of the user who made the edit.
* \{{edited range\}}: The notation (string) of the cell being edited.
* \{{column A\}}: All values in column A(dynamic).
* \{{row 1\}}: All values in row 1(dynamic).
* \{{sheet\}}: The name of the sheet that was edited or set in the trigger step.
* \{{spreadsheet url\}}: The URL of the spreadsheet that this automation belongs to.
* \{{automation name\}}: The name of the automation workflow you have set.
* \{{form values\}}: All values of the form submission that was received.
* \{{form values 1\}}: The first value (or the nth value if you set the number as n) of the form submission that was received.
{% endhint %}
