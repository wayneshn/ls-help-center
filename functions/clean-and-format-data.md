# Clean and format data

### **Remove duplicate rows**

This function will simply remove all extra rows that have the same value in each cell. Only one duplicate row will be preserved.

### Change text casing

This function will change the text casing of all values of the selected range.

**Data range:** Select the data range. A range represents a single cell or a group of adjacent cells in your spreadsheet. For example, A1:D10 is shown below.

<figure><img src="../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

**Case type:** Select the desired case type from the list. Currently we support the following types:

* Upper case (THIS IS UPPERCASE
* Lower case (this is lower case)
* Proper case (This Is Proper Case)
* Sentence case (This is sentence case)
* Upper camel case, or pascal case (ThisIsUpperCamelCase)
* Lower camel case (thisIsLowerCamelCase)
* Train case (This-Is-Train-Case)
* Snake case (this\_is\_snake\_case)
* Kebab case (this-is-kebab-case)

### Round numbers

This function will round all numbers to the nearest integers.

**Data range:** Select the data range. A range represents a single cell or a group of adjacent cells in your spreadsheet. For example, A1:D10 is shown below.

<figure><img src="../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

### Clean data

This function allows you to clean data in the selected range. For example, you can remove all punctuations from text values.

**Data range:** Select the data range. A range represents a single cell or a group of adjacent cells in your spreadsheet. For example, A1:D10 is shown below.

<figure><img src="../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

**Option:** How do you want your data to be clean? We support the following types:

* Remove lead spaces. This will remove leading spaces from all cells in the selected range.
* Remove trailing spaces. This will remove trailing spaces from all cells in the selected range.
* Remove all non-numbers. This will remove all values that are not numbers from all cells in the selected range. For example: “He is 30 years old.” will become “30”.
* Remove all numbers: This will remove all values that are numbers from all cells in the selected range. For example: “He is 30 years old.” will become “He is 30 years old.”.
* Remove all punctuations. This will remove all punctuations from all cells in the selected range. For example: “He is 30 years old, isn’t he?” will become “He is 30 years old isnt he”.

### Unpivot data

This function will transform a pivot table into raw data. Read more [here](https://docs.tibco.com/pub/spotfire/6.5.1/doc/html/data/data\_unpivoting\_data.htm).

**Data range:** Select the data range. A range represents a single cell or a group of adjacent cells in your spreadsheet. For example, A1:D10 is shown below.

![Data range example in Google Spreadsheets](<../.gitbook/assets/image (71).png>)

### Unix time converter

This function will convert epoch time/UNIX timestamps into the UTC time. This is useful when you have retrieved a column of timestamps from an API endpoint that uses the UNIX timestamp.

**Data range:** Select the data range. A range represents a single cell or a group of adjacent cells in your spreadsheet. Only one column each execution is allowed.

