# Tableau



Here are the step-by-step instructions to connect the sample MySQL database to Tableau and create the specified visualization. If you haven't set up MySQL and populated it with the sample data yet, I have a dedicated section for that at 

https://github.com/ramandcpu/SQL/tree/main/mysql

Once you have the MySQL database ready, follow these instructions to connect it to Tableau and build the visualization:

## Connect MySQL Database to Tableau

1. Open Tableau Desktop and under "Connect", select "MySQL".

If this is the very first time after installing Tableau, after clicking on "MySQL" in the data source list, you will be asked to install the MySQL ODBC connector. Just follow the on-screen instructions provided by Tableau, which will guide you to the required MySQL Connector/ODBC download site for Windows. Click the link provided by Tableau to install the connector, and then you can proceed with connecting Tableau to your MySQL database.

https://dev.mysql.com/downloads/connector/odbc/



    After installing Tableau Desktop, you launch it for the first time.
    You select "MySQL" as the data source to connect to.
    Tableau detects that the MySQL ODBC connector is not installed on your system.
    Tableau will display a message prompting you to install the MySQL ODBC connector.
    Follow the on-screen instructions provided by Tableau to install the connector.
    Tableau will provide a link to the MySQL Connector/ODBC download page.
    Download and install the MySQL Connector/ODBC for your Windows operating system.
    Once the installation is complete, you can proceed with connecting Tableau to your MySQL database.


<img src="/part-1/pics/pic-1.png" width="500" />

3. Enter the name of the server that hosts the MySQL database you populated with the sample data from https://github.com/datacharmer/test_db.

<img src="/part-1/pics/pic-2.png" width="500" />

5. Enter your MySQL user name and password.

6. Select the "Employees" database from the list or search for it by name.

7. Under "Tables", select the "employees", "dept_emp", and "salaries" tables.

8. Drag the "employees" table to the canvas to start setting up the data source.

9. Drag the "dept_emp" and "salaries" tables to the canvas and join them to the "employees" table based on the "emp_no" column.

10. Select the "Sheet 1" tab to begin your analysis.

The benefit of connecting Tableau to MySQL is that we can perform a lot of calculations and data extraction directly within Tableau. However, to utilize this functionality, you will need the Tableau Professional version. If you have the Tableau Public version, you would need to preprocess the data in MySQL and export it as a CSV file before importing it into Tableau. With the setup you described, where you have populated the sample MySQL database, you can take advantage of Tableau's ability to perform calculations and extractions on the data stored in MySQL without the need for any preprocessing or exporting to CSV.

.

.

<img src="/part-1/pics/pic-3.png" width="500" />
.

.

<img src="/part-1/pics/pic-4.png" width="500" />
.

.

<img src="/part-1/pics/pic-5.png" width="500" />


## Create the Visualization

1. In the "Columns" shelf, drag the "hire_date" field from the "employees" table.

2. In the "Rows" shelf, drag the "emp_no" field from the "employees" table.

3. In the "Marks" card, change the mark type to "Circle".

4. Drag the "gender" field from the "employees" table to the "Color" shelf in the "Marks" card.

5. Drag the "gender" field from the "employees" table to the "Detail" shelf in the "Marks" card.

6. Drag the "salary" field from the "salaries" table to the "Label" shelf in the "Marks" card.

7. Adjust the size of the circles and labels as needed for better visibility.

8. (Optional) Add a title, axis labels, and other formatting to enhance the visualization.

9. Select "Fit" from the "Size" dropdown in the toolbar to fit the entire view on the canvas.

10. The final visualization will show a scatter plot of employees based on their hire date and employee number, with circles colored by gender and salary amounts displayed as labels.

By following these steps, you can successfully connect the sample MySQL database to Tableau and create the specified visualization using the "employees", "dept_emp", and "salaries" tables.


Alright, after this, I'll share a screenshot of my setup along with the specific values that need to be modified to replicate your desired charts and configuration. Providing a visual representation is more effective than a lengthy textual explanation, especially since the process primarily involves drag-and-drop actions and clicking on various options. Showing the actual setup visually is more efficient and easier for readers to follow. So, without further ado, here's my setup:

.

.

<img src="/part-1/pics/pic-6.png" width="500" />
.
.

.
<img src="/part-1/pics/pic-7.png" width="500" />
.
.

.
<img src="/part-1/pics/pic-8.png" width="500" />
.
.

.
<img src="/part-1/pics/pic-9.png" width="500" />
.
.

.
<img src="/part-1/pics/pic-10.png" width="500" />
.
.

.
<img src="/part-1/pics/pic-11.png" width="500" />
.
.

.
<img src="/part-1/pics/pic-12.png" width="500" />
.
.
.
<img src="/part-1/pics/pic-13.png" width="500" />
.

.









