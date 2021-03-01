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
SET GLOBAL general_log=ON;
</pre>