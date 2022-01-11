<h1>MySql</h1>

<h2>MySQL Server Administration</h2>

<h3>The General Query Log</h3>
It's a general log of what mysqld is doing. <br>

Official documentation: <br>
<a href="https://dev.mysql.com/doc/refman/8.0/en/query-log.html" target="_blank">https://dev.mysql.com/doc/refman/8.0/en/query-log.html</a><br>
<br>
Get location of general log file on server. <br>
<pre>show variables like '%general%';</pre>
<br>
<pre>
See all executed SQL queries
SELECT * FROM mysql.general_log;

Activate general log
SET global general_log = 1;
SET global log_output = 'table';Reset the general_log table
SET GLOBAL general_log=OFF;

TRUNCATE table mysql.general_log;
SET GLOBAL general_log=ON;</pre>

<br>
<h3>The Binary Log</h3>
Documentation
<a href="https://dev.mysql.com/doc/refman/8.0/en/binary-log.html" target="_blank">https://dev.mysql.com/doc/refman/8.0/en/binary-log.html</a><br>

It contains "events" that describe database changes such as table cration or changes to table data. <br>

- It can be used for Certain data recovery opertaions such as re-executing recored binary logs to brung databases up to date from the point of the backup. <br>

<br>
Read binary files in the following way<br>
<pre>
mysqlbinlog bin.000001 | less
</pre><br>
<br>
The binary log is NOT used for statments such as SELECT or SHOW that do not modify data. To log all statements (for example to identify a problem query) use the general query log. <br>

<br>
<h3>The MySql Socket</h3>
The MySql socket path can be found in the following way <br>
<pre>show variables like 'socket';</pre>
