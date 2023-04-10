# Get data

### Get data from a database

This function allows you to pull data from an external MySQL database. You can only retrieve data from one table of the database each time. The data will be inserted starting from the cell which your cursor has selected.

In order to create a database connection using the JDBC service used by this function, you must allow certain IP ranges in your database settings to allow Google Apps Script to access it. These are the [IP address ranges](https://www.gstatic.com/ipranges/goog.txt) you’ll need to allow list.

**Database type:** The function currently supports MySQL, Google Cloud SQL MySQL, Microsoft SQL Server, and Oracle databases.

**Database URL:** The URL/Hostname address of the database, without port.

**Database port** Port of the database. The JDBC service used by this function can only connect to ports 1025 and above. Ensure your database is not serving off a lower port.

**Database name:** The name of the database to retrieve data.

**Table name:** The name of the table in the database to retrieve data.

### Get data from a webpage

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

**Webpage url:** The webpage url where the desired data is located.

**Data type:** Select the type of desired structured data. It can be a table content or a list on the webpage.

**Data index:** The index, starting at 1, which identifies which table or list as defined in the HTML source should be returned. (The indices for lists and tables are maintained separately, so there may be both a list and a table with index 1 if both types of elements exist on the HTML page.)
