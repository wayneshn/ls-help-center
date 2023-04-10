# Work with APIs

### Pull from an API

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

**Method:** Choose the HTTP method to pull data from an API endpoint. Currently, we only support the GET and POST methods. If you want to use other HTTP methods like PUT, DELETE and PATCH, please use the [LogicSheetAPI formula](the-logicsheetapi-formula.md#how-to-use-logicsheetapi). Please check your API reference to decide which method you want to use.

**API URL:** Type in the URL and full path of the API endpoint, including all parameters. Parameters are usually used to pass in API keys for simple authentication methods.

For example: https://mydata.com/api/v2/dataset1?para1=value1\&api\_key=keyvalue

**Headers:** Headers let you pass additional information with the API request. Request headers can be used in the request to provide information about the request context to help the server tailor the response. You can use, for example, the Authorization header to provide authentication credentials.

If the server responded with a 401 Unauthorized status, usually you should provide credentials to authenticate the request. To do so, you will need to use the Authorization header.

The value of the Authorization header should be :

```
<type> <credentials>
```

_Common types_:

* Basic: Base64-encoded credentials.
* Bearer: Bearer tokens to access OAuth 2.0-protected resources

**Path:** If provided, the function will only retrieve data that is located in the path. For example, You can enter key1.key2\[1].key3 to retrieve to the value of key3 of the second object of array key2 of the object key1.

If the JSON response looks like this:

```json
{
    "id": 1001,
    "person": [
        {
            "name": "John",
            "age": 45,
            "city": "New York"
        },
        {
            "name": "Rich",
            "age": 34,
            "city": "London"
        }
    ]
}
```

the path person\[1].name will return “Rich”, while the path person\[0] will return all information about John.

**Request body:** Enter the JSON format request body. This will only apply to the POST method. For example, when creating a resource using POST, the request body usually contains the representation of the resource to be created.

### Enrich with an API



**Column number:** Type in the number of columns of the data to be processed. For example, column C should be 3.

**Start row:** Type in the number of the start row of the data to be processed.

This function will only process a column of data, so you have to choose which column and from which row you want the data to be processed. This is an example

**Method:** Choose the HTTP method to send data to an API endpoint. Currently, we only support the GET and POST methods, though we will add more. Please check your API reference to decide which method you want to use.

**API URL:** Type in the URL and full path of the API endpoint, including all parameters. Parameters are usually used to pass in API keys for simple authentication methods.

You can also include \{{merge\_tag\}} in the url parameters to represent data from the sheet to be sent to the API endpoint.

For example: https://mydata.com/api/v2/dataset1?api\_key=keyvalye\&data=\{{merge\_tag\}}

**Headers:** Headers let you pass additional information with the API request. Request headers can be used in the request to provide information about the request context to help the server tailor the response. You can use, for example, the Authorization header to provide authentication credentials.

If the server responded with a 401 Unauthorized status, usually you should provide credentials to authenticate the request. To do so, you will need to use the Authorization header.

The value of the Authorization header should be :

```
<type> <credentials>
```

_Common types_:

* Basic: Base64-encoded credentials.
* Bearer: Bearer tokens to access OAuth 2.0-protected resources

**Path:** If provided, the function will only retrieve data that is located in the path. For example, You can enter key1.key2\[1].key3 to retrieve to the value of key3 of the second object of array key2 of the object key1.

If the JSON response looks like this:

```
{
    "id": 1001,
    "person": [
        {
            "name": "John",
            "age": 45,
            "city": "New York"
        },
        {
            "name": "Rich",
            "age": 34,
            "city": "London"
        }
    ]
}
```

the path person\[1].name will return “Rich”, while the path person\[0] will return all information about John.

**Request body:** Enter the JSON format request body. This will only apply to the POST method. For example, when creating a resource using POST, the request body usually contains the representation of the resource to be created. use \{{merge\_tag\}} to represent data from the sheet to be sent to the API endpoint.

For example:

```
{
    "data": {{merge_tag}},
    "process": true
}
```
