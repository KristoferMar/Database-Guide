<h1>Database-Guide</h1>
MySQL, SQL Commands, noSQL db's, DB commands and much more.

<h2>General SQL information</h2>
SQL is a standard language for accessing and manipulating databases. <br>

Introduction to Mysql: <br>
<a href="https://github.com/KristoferMar/Database-Guide/blob/master/SQL-Info.md" target="_blank">https://github.com/KristoferMar/Database-Guide/blob/master/SQL-Info.md</a><br>

<h3>SQL </h3>


<h2>Mysql</h2>
Detect if you have MySQL installed with <br>
<i><b> mysql --version </b></i><br>

Find location to MySQL and it's services <br>
<i><b>which mysql</b></i><br>

<br>
<h3>MySQL Keywords</h3>
<h4>SELECT Query</h4>
The SQL SELECT command is used to fetch data from the MySQL database. 
```
SELECT field1, field2 FROM table_name;
```

<h4>SET</h4>
The SET command is used with UPDATE to specify which columns and values that should be updated in a table. <br>

```
UPDATE Customers SET ContactName = 'Kristofer Mar', City= 'Cophenhagen' WHERE CustomerID = 1;
```



<br>
<h2>SQL Commands</h2>

Get all available tables <br>
<i>Select * from INFORMATION_SCHEMA.TABLES; </i><br>

Show all users <br>
<i>SELECT * FROM mysql.user;</i><br>



<br>
<h3>Search for keyword</h3>
You can search for a string keyword in any column the following way <br>
<i> SELECT * FROM mytable WHERE column1 LIKE '%word1%' OR column1 LIKE '%word2%'</i><br>



<br>
<h4>SQL Dump</h4>
- By default, sqldump produces a set of SQL statements that can be executed to reproduce the original database object definitions and table data. You can save the output in a file in the following way: <br>
<b><i>mysqldump --user=wikiadmin --password=wikipw --host=db.mywiki.com wikidb > wikidb.sql</i></b><br>

<br>
<h2> Flyway </h2>

It works like git.. It's a version control for your database.