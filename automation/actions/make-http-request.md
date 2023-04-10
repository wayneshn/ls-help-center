---
description: Make an HTTP request as an automation action.
---

# Make HTTP request

The HTTP request action type allows you to make an HTTP request to a URL once the workflow is triggered and all conditions are met.

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption><p>Automatically send an HTTP request from Google Sheets</p></figcaption></figure>

{% hint style="info" %}
#### Merge tag available

You can use merge tags in any fields in the HTTP request form to refer to dynamic data in your spreadsheet. See how to use [merge tags](../merge-tags.md) here.
{% endhint %}

In the following example, we will go through how to make a POST request and test it.

First, choose an HTTP method and fill in the URL. In this example, we chose the POST method.

Optionally, you can add request parameters to the request.

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

You can also add headers and a JSON request body if applicable.

<figure><img src="../../.gitbook/assets/image (91).png" alt=""><figcaption><p>Add request headers</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (54).png" alt=""><figcaption><p>Add a JSON request body</p></figcaption></figure>

Once you have completed configuring your HTTP request, you can send a test request by clicking the "Test" button.

{% hint style="warning" %}
Please note that merge tags will not be transformed if you test the HTTP request. Currently, merge tags will only be transformed when the action is triggered in an automation. The test step here is only used to test if the request is successful.&#x20;
{% endhint %}

Once you have hit the "Test" button, you will be able to see the test response.

<figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

And in the backend of the request server, we can see the logs.

<figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

### Example

Now let's try the action with a real-world example. Say we have a Google form linked with a spreadsheet and every time a form response is received, we want to send the form data to an API endpoint.

Here are the questions in the Form.

&#x20;

<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

And here is how the spreadsheet receiving form requests is set up.

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

Let's make a new automation in Logic Sheet.

In the trigger step, choose the "A form response is received" trigger, and, in this example, choose "Form Responses 1" as the sheet.

We will set no conditions in the example. But if you want to, check the [conditions](../conditions.md) help article.

In the action step, add a new action and choose the "Send an HTTP request" action type.

In this example, we will use the Beeceptor mock API. Requests sent to the mock API endpoint will be logged in Beeceptor's backend.

We will set no parameters and headers in this example, but use the request body to send the form data to the API.

In the JSON request body, we will use merge tags like this:

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

In the JSON request body, we used merge tags to indicate the upcoming form response values. \{{form response 1\}} is the first value of the form response we receive, thus it is the timestamp. The same applies to other values.

Now we can save the automation and submit a form response.

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

Once the form is submitted, the values will be added to the spreadsheet.

<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

And on Beeceptor's backend, we can see that the form values are passed through.

<figure><img src="../../.gitbook/assets/image (68).png" alt=""><figcaption><p>Sending form values to API</p></figcaption></figure>
