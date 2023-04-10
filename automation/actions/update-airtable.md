---
description: Update a table in your Airtable.
---

# Update Airtable

In order to use this automation action, you will also have to [connect your Google Sheets with Airtable](../add-connections/airtable-connection.md) first.

To use the update Airtable action, you first need to make a new automation by clicking on the _New automation_ button in your Logic Sheet sidebar. In this tutorial, I will simply use the “_Spreadsheet is edited_” trigger and choose to not set any conditions.

In the action step, choose the “_Create new Airtable record_” action. Please note that if you haven’t connected your Airtable account, this option will not be available.

Now let's do the same thing by copying the table link and pasting it into the Airtable table link input.

![Airtable Google Sheets integration automation](https://static.logicsheet.co/img/site/airtable-intro/airtable-action-0.png)

Now that we have the link, we need to click on the _Fetch fields_ button to fetch all the fields (think of column names in sheets) from Airtable.

![](https://static.logicsheet.co/img/site/airtable-intro/airtable-action-2.png)

Now let’s fill the fields in with some data. You can of course use static data, but chances are that you want to use dynamic data in your Google Sheets in these fields. In this example, I will just try to pass the value that I edited and the range of the edited cell to Airtable using merge tags.&#x20;

Merge tags are values that are wrapped in double curly braces that Logic Sheet uses to pass dynamic data in Google Sheets. Read more about [merge tags](../merge-tags.md) here.

So the configuration will be like

![Airtable Google Sheets automation connection](https://static.logicsheet.co/img/site/airtable-intro/airtable-action-3.png)

Now let’s preview and save the new automation. Once it’s saved, let’s make a new edit at cell A1.

![Airtable Google Sheets](https://static.logicsheet.co/img/site/airtable-intro/airtable-action-4.png)

And let’s check the Airtable to see if the new record has been added. And yes, it has been appended to the last row.

![Google Sheets Airtable integration](https://static.logicsheet.co/img/site/airtable-intro/airtable-action-5.png)

This is just a simple example of how you can send dynamic data in Google Sheets to Airtable. Using our powerful [merge tags](https://help.logicsheet.co/automation/merge-tags), you can make your requests way more dynamic.
