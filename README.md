# Database-Guide
MySQL, SQL Commands, noSQL db's, DB commands and much more.

## SQL Commands

Get all available tables <br>
<b><i>Select * from INFORMATION_SCHEMA.TABLES; </i></b>

SQL Dump
- By default, sqldump writes information as SQL statements to the standard output. You can save the output in a file:
<b><i>mysqldump --user=wikiadmin --password=wikipw --host=db.mywiki.com wikidb > wikidb.sql</i></b>
