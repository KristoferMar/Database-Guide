# Database-Guide
MySQL, SQL Commands, noSQL db's, DB commands and much more.

<h2>General SQL information</h2>
Introduction to Mysql: <br>
<a href="https://github.com/KristoferMar/Database-Guide/blob/master/SQL-Info.md" target="_blank">https://github.com/KristoferMar/Database-Guide/blob/master/SQL-Info.md</a><br>


<h2>Mysql</h2>
Detect if you have MySQL installed with <br>
<i><b> mysql --version </b></i><br>

Find location to MySQL and it's services <br>
<i><b>which mysql</b></i><br>


## SQL Commands

Get all available tables <br>
<b><i>Select * from INFORMATION_SCHEMA.TABLES; </i></b>

SQL Dump
- By default, sqldump produces a set of SQL statements that can be executed to reproduce the original database object definitions and table data. You can save the output in a file in the following way:
<b><i>mysqldump --user=wikiadmin --password=wikipw --host=db.mywiki.com wikidb > wikidb.sql</i></b>

# Flyway

It works like git.. It's a version control for your database.
