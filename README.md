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
    In this next example, we will focus in on the date of 05-09-2022 as the date a suspicious even occurred. We will run a request in SQL to review all log in attempts that had occurred between 05-08-2022 and 05-09-2022 to better picture of the events that occurred.<br>
        We will use the query SELECT * FROM log_in_attempts WHERE login_date = ’22-05-09’ or login_date = ’22-05-08’; 
We can review all 75 instances of both failed and successful log-in attempts between 05-08-2022 and 05-09-2022.
<br>
        <img src="https://github.com/jagilmorProf/SQL/blob/main/Picture2.png">
    <p>
        Overall, as a cybersecurity professional it is important to understand the core concept of SQL to allow yourself to be able to fully unlock the entire toolkit of Filters and outputs that the database will provide. Understanding filters will assist cybersecurity professionals in better understanding the data provided and allows for users to hone in on details that will make their organization's databases and networks formidable entities.
    </p>
</body>
</html>
