# SQL
<!DOCTYPE html>
<html lang="en">
<body>
    <h1>Apply filters to SQL queries</h1>
    <h2>Project description</h2>
    <p>
        In this document we will demonstrate the interaction between a cybersecurity expert and SQL databases. In this scenario we will be looking at discovering possible security issues involving log-in attempts and employee machines. We will review data from an organization database, and use various filter functions such as AND, OR, and NOT to allow for easier consumption and assessment of data gathered from the database.
    </p>
    <h3>Retrieve after hours failed login attempts</h3>
    <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture1.png">
    <p>
        In this request, we asked the MariaDB to look in the organization database, within the log_in_attempts table to find all log-ins that happened after 6:00 PM, and all of the attempts that resulted in a failure “0” result.
  <br>
    We can see that there are 19 different attempts shown in this result.
          </p>
 <h2>Retrieve login attempts on specific dates</h2>
    <p>
    In this next example, we will focus in on the date of 05-09-2022 as the date a suspicious even occurred. We will run a request in SQL to review all log in attempts that had occurred between 05-08-2022 and 05-09-2022 to better picture of the events that occurred.<br><br>
        We will use the query SELECT * FROM log_in_attempts WHERE login_date = ’22-05-09’ or login_date = ’22-05-08’; 
We can review all 75 instances of both failed and successful log-in attempts between 05-08-2022 and 05-09-2022.
<br><br>
        <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture2.png">
    <p>
        <h3>Retrieve login attempts on outside of Mexico</h3><br>
        In this next query we will run a request to find all log_in_attempts that have not been attempted in Mexico. We will use the line SELECT * FROM log_in_attempts WHERE NOT country LIKE ‘MEX%’;
We will use the % wild card to assume all entries that are from “MEX” and “MEXICO” both mean Mexico.
<br>
     <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture3.png"><br>
     <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture4.png"><br>
        We ended up with 144 results which are all of the login attempts that occurred outside of Mexico.<br></p>
    <h4>Retrieve login attempts on outside of Mexico</h4><br>
 <p>   Next we will look at all employees in the Marketing department. We will be using the employees table. We will query using the following request:
SELECT * FROM employees WHERE department = ‘Marketing’;<br>
     <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture5.png"><br></p>
    <h5>Retrieve employees in Finance or Sales</h5><br>
<p>Very similar to the previous example of filtering just one department, we will instead look at Finance or the Sales department. 
We will query with the following request:
SELECT * FROM employees WHERE department = ‘Finance’ OR department = ‘Sales’;<br>
    <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture6.png"><br></p>
 <h6>Retrieve all Employees not in IT</h6><br>
<p>Lastly in the employees table we will query all employees that are not in the IT department with the following query:<br>
    <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture7.png"><br>
    <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture8.png"><br>
    The query results in 161 results, only showing the departments that are all except ‘Information Technology’</p><br>
    <h7>Summary</h7><br>
    <p>
        Overall, as a cybersecurity professional it is important to understand the core concept of SQL to allow yourself to be able to fully unlock the entire toolkit of Filters and outputs that the database will provide. Understanding filters will assist cybersecurity professionals in better understanding the data provided and allows for users to hone in on details that will make their organization's databases and networks formidable entities.
    </p>
</body>
</html>
