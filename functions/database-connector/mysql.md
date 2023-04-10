# MySQL

In this article, we will go through how to use [Logic Sheet](https://logicsheet.co/) to connect your spreadsheet with a MySQL database. Logic Sheet has a custom formula that allows you to write SQL queries from any cell in a spreadsheet and retrieve data from a database.

### Setting up connections between Google Sheets and MySQL

Once you have opened the Logic Sheet add-on, you can start typing in any cell in your worksheet to call the Logic Sheet MySQL formula. All Logic Sheet formulas start with the combination LogicSheet, so if you start typing =LogicSheet in any cell, you will see a range of Logic Sheet formulas.

![Logic Sheet formulas](https://static.logicsheet.co/img/site/article-sheet-mysql/logicsheet-formulas.png)

Note that there are two MySQL-related formulas. The LogicSheetMySQLTable formula will pull data from a table in your database and it doesn’t need you to write any SQL queries. You can imagine this is a simpler version of the LogicSheetMySQL formula.

The formula we are going to use the most is the LogicSheetMySQL formula, in which you can not only pull data from the database but also send data from your Google Sheets to a database.

In order to connect to a MySQL database, you need to prepare the following information.

* Database URL (or IP address)
* Database port number
* Database user name
* Database password
* Database name

Like other Google Sheets formulas, you can refer to values that are stored in other cells in a formula cell. In this case, we will store the credentials in the first and second rows so that we can refer to them in later formula calls.

![LogicSheetMySQL get data from MySQL to Google Sheets](https://static.logicsheet.co/img/site/article-sheet-mysql/logicsheetmysql-firstcall.png)

Now that we have provided all the credentials needed to connect to the test database created using _db4free.net_, we need to write a SQL query to tell the database what we need. I have previously created some dummy data in the test database in a table called users. Let’s try pulling data from the users table using the SQL query SELECT \* FROM users.

And voila, we have all the data from the users table in the test database in our Google Sheets.

![Select a table from MySQL database to Google Sheets](https://static.logicsheet.co/img/site/article-sheet-mysql/select-from-all-users.png)

### Run complex queries

In the last section, we successfully connected Google Sheets to the test MySQL database. But in order to run more complex queries, we also need to use references. This, on the one hand, can help us escape double quotes. On the other hand, it allows us to include dynamic data in the query so that we can interact with the database using data in Google Sheets.

In the following example, I will try to send a row of data from Google Sheets to the users table of the MySQL database.

![](https://static.logicsheet.co/img/site/article-sheet-mysql/bob-raw.png)

In the example, I will try to send a new user row (Bob) to the database.

In order to more conveniently refer to the data, I will use cell D5 to build the SQL query that contains data from A5 to C5. The query should be as follow:

```sql
INSERT INTO users (name, email, age)
VALUES ('Bob', 'bob@example.com', '36');
```

In this case, we will use the =CONCATENATE formula in Google Sheets to build the SQL query.

![](https://static.logicsheet.co/img/site/article-sheet-mysql/bob-concat.png)

The formula should return the right query in cell D5 like this.

![](https://static.logicsheet.co/img/site/article-sheet-mysql/bo-finanl.png)

After building the query, we will be able to send the query to the MySQL database using the LogicSheetMySQL formula.

![](https://static.logicsheet.co/img/site/article-sheet-mysql/bob-mysql-call.png)

The formula returns a “Done” in cell D5 and which means it has successfully sent the data to the database.

Let’s check the users table using the same formula. And the user Bob is in the database!

![](https://static.logicsheet.co/img/site/article-sheet-mysql/mysql-bob-done.png)

In the above examples, we covered how to pull and push MySQL data from Google Sheets using [SQL verbs](https://www.w3schools.com/sql/sql\_quickref.asp) like SELECT and INSERT. We can already imagine what else we can do with the LogicSheetMySQL formula.

For example, we can search for particular data using the WHERE statement and remove data using the DELETE verb. There is no limit to what you can do if you know how to write effective SQL queries.

### Whitelist Google service IPs

The LogicSheetMySQL formula uses Google Apps Script’s JDBC service to connect to MySQL databases. Sometimes, your database may have a firewall that blocks requests from unknown IP addresses.&#x20;

In order to create a database connection using the LogicSheetMySQL formula, you must allow-list certain IP ranges in your database settings to allow the JDBC service to access it. These are the address ranges you'll need to [allow-list](https://www.gstatic.com/ipranges/goog.txt).
