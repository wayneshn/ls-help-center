---
description: >-
  Use the =LogicSheetAPI custom function to import API directly to your
  worksheet using cell formulas.
---

# The LogicSheetAPI formula

### How to use =LogicSheetAPI?

{% hint style="info" %}
If you want to use the =LogicSheetAPI function in a new spreadsheet, you have to launch the Logic Sheet add-on at least once in that spreadsheet. The add-on can be found in the Add-on menu. If you haven't installed Logic Sheet yet, click [here](https://workspace.google.com/marketplace/app/logic\_sheet\_data\_processing\_data\_analysi/796322869198) to install.
{% endhint %}

Call the LogicSheetAPI custom function by typing =LogicSheetAPI in any cell. Now you will see a list of parameters to fill in to use the function. You will also be able to see the documentation inside your Google Sheets. If the documentation doesn't show up, just click the question mark(?) next to the function name.

#### Parameters

Here are the parameters you can use to call LogicSheetAPI.

{% hint style="info" %}
It's a good practice to store parameter content in separate cells for later reference. It will also help you escape quotations markets if you want to include a JSON request body.
{% endhint %}



* **method:** The HTTP request method for the API request. It can either be "GET" or "POST".
* **url:** The URL of the API endpoint. You can also include request parameters in the URL.
* **path:** _\[optional]_ A list of paths to be imported. For example: "/first\_name, /email" will only import data under the "first\_name" and "email" paths. If you don't want to specify the path, just use "" in the parameter to escape it.
* **header:** _\[optional]_ The request header should be a comma-separated list of header items. You can use it to pass authentications. For example: "apikey=YOUR\_API\_KEY,content-type=application/json". No space before or after commas.
* **requetBody**: _\[optional]_ For the POST method only. The request body sent to the API endpoint. Type in JSON format if you are using application/json.

#### Here is an example GET request

{% swagger method="get" path="?limit=3" baseUrl="https://api.thecatapi.com/v1/votes" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="x-api-key" type="DEMO-API-KEY" %}

{% endswagger-parameter %}

{% swagger-parameter in="header" name="content-type" type="application/json" %}

{% endswagger-parameter %}
{% endswagger %}

This is how you can make the GET request using LogicSheetAPI.

```
=LogicSheetAPI("GET", "https://api.thecatapi.com/v1/votes", "", "x-api-key=f2b451ef-af64-49d4-8594-378ee24ae040,content-type=applic
ation/json")
```

This is an example of the LogicSheetAPI working on Google Sheets. Parameters are stored in separate cells.

![GET request using LogicSheetAPI function](<../../.gitbook/assets/image (24).png>)

This is an example result:

![GET response using LogicSheetAPI function](<../../.gitbook/assets/image (77).png>)

#### Here is an example POST request

{% swagger method="post" path="/" baseUrl="https://api.thecatapi.com/v1/votes" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" type="DEMO-API-KEY" name="x-api-key" %}

{% endswagger-parameter %}

{% swagger-parameter in="header" type="application/json" name="content-type" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" required="false" type="the_image_id" name="image_id" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="sub_id" type="my-user-1234" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="value" type="3" %}

{% endswagger-parameter %}
{% endswagger %}

This is how you can make the POST request using LogicSheetAPI.

```
=LogicSheetAPI("POST", "https://api.thecatapi.com/v1/votes", "", "x-api-key=DEMO-API-KEY,content-type=applic
ation/json", D2)
```

{% hint style="info" %}
In this example, we use cell D2 to store the request body in order to escape the quotation marks in the JSON string.
{% endhint %}

This is an example of the LogicSheetAPI working on Google Sheets. Parameters are stored in separate cells.

![POST response using LogicSheetAPI function](<../../.gitbook/assets/image (37).png>)
