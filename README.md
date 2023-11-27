<!DOCTYPE html>
<html lang="en">
<body>
    <h1>SQL</h1>
    <h2>Apply filters to SQL queries</h2>
    <h3>Project description</h3>
    <p>
        In this document, we will demonstrate the interaction between a cybersecurity expert and SQL databases. In this scenario, we will be looking at discovering possible security issues involving log-in attempts and employee machines. We will review data from an organization database and use various filter functions such as AND, OR, and NOT to allow for easier consumption and assessment of data gathered from the database.
    </p>
    <h3>Retrieve after-hours failed login attempts</h3>
    <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture1.png">
    <p>
        In this request, we asked the MariaDB to look in the organization database, within the log_in_attempts table, to find all log-ins that happened after 6:00 PM and all of the attempts that resulted in a failure “0” result.
        <br>
        We can see that there are 19 different attempts shown in this result.
    </p>
    <h3>Retrieve login attempts on specific dates</h3>
    <p>
        In this next example, we will focus on the date of 05-09-2022 as the date a suspicious event occurred. We will run a request in SQL to review all log-in attempts that occurred between 05-08-2022 and 05-09-2022 to better picture the events that occurred.
        <br><br>
        We will use the query: <code>SELECT * FROM log_in_attempts WHERE login_date = '22-05-09' OR login_date = '22-05-08';</code>
        <br><br>
        We can review all 75 instances of both failed and successful log-in attempts between 05-08-2022 and 05-09-2022.
        <br><br>
        <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture2.png">
    </p>
    <h3>Retrieve login attempts outside of Mexico</h3>
    <p>
        In this next query, we will run a request to find all log_in_attempts that have not been attempted in Mexico. We will use the line: <code>SELECT * FROM log_in_attempts WHERE NOT country LIKE 'MEX%';</code>
        <br>
        We will use the % wildcard to assume all entries that are from “MEX” and “MEXICO” both mean Mexico.
        <br>
        <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture3.png">
        <br>
        <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture4.png">
        <br>
        We ended up with 144 results, which are all of the login attempts that occurred outside of Mexico.
    </p>
    <h3>Retrieve employees in Marketing</h3>
    <p>
        Next, we will look at all employees in the Marketing department. We will be using the employees table. We will query using the following request:
        <br><code>SELECT * FROM employees WHERE department = 'Marketing';</code>
        <br>
        <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture5.png">
    </p>
    <h3>Retrieve employees in Finance or Sales</h3>
    <p>
        Very similar to the previous example of filtering just one department, we will instead look at Finance or the Sales department.
        <br>
        We will query with the following request:
        <br><code>SELECT * FROM employees WHERE department = 'Finance' OR department = 'Sales';</code>
        <br>
        <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture6.png">
    </p>
    <h3>Retrieve all employees not in IT</h3>
    <p>
        Lastly, in the employees table, we will query all employees that are not in the IT department with the following query:
        <br>
        <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture7.png">
        <br>
        <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture8.png">
        <br>
        The query results in 161 results, only showing the departments that are all except ‘Information Technology’.
    </p>
    <h3>Summary</h3>
    <p>
        Overall, as a cybersecurity professional, it is important to understand the core concept of SQL to allow yourself to be able to fully unlock the entire toolkit of filters and outputs that the database will provide. Understanding filters will assist cybersecurity professionals in better understanding the data provided and allows for users to hone in on details that will make their organization's databases and networks formidable entities.
    </p>
</body>
</html>
