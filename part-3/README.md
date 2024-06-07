# Connect to CSV files In Tableau


First of all we will extract `employees`, `departments`, and `dept_emp` tables as CSV files in MySQL Workbench. You can use the following tutorial if needed help;

https://github.com/ramandcpu/SQL


Extracting the `employees`, `departments`, and `dept_emp` tables as CSV files in MySQL Workbench, using the method without right-clicking for export:

### Step-by-Step Instructions

#### 1. Open MySQL Workbench and Connect to Your Database

1. Open MySQL Workbench.
2. Connect to your MySQL database by clicking on the appropriate connection, in our case we have only one setup.

#### 2. Select the Database

1. In the SQL Editor, type the following command to use the desired database (replace `employees` with the actual database name):

```sql
USE employees;
```

2. Execute the command by clicking the lightning bolt icon or pressing `Ctrl + Enter`.

#### 3. Write and Execute the SELECT Statements

1. Open a new SQL tab by clicking on the "SQL +" button.
2. Write the SELECT statements for each table:

```sql
-- For employees table
SELECT * FROM employees;

-- For departments table
SELECT * FROM departments;

-- For dept_emp table
SELECT * FROM dept_emp;
```

<img src="/part-3/pics/tab_mysql-1.png" width="500" />

<img src="/part-3/pics/tab_mysql-2.png" width="500" />

<img src="/part-3/pics/tab_mysql-3.png" width="500" />


3. Execute each SELECT statement by clicking the lightning bolt icon or pressing `Ctrl + Enter`.

#### 4. Export the Results to CSV

1. **Export `employees` Table:**
   - After executing the SELECT statement for the `employees` table, you will see the results in the Result Grid.
   - Click on the "Export" button located above the Result Grid.
   - In the "Export Data" dialog, select "CSV" as the format.
   - Choose a location to save the CSV file, name it `employees.csv`, and click "Save".

2. **Export `departments` Table:**
   - Execute the SELECT statement for the `departments` table.
   - Click on the "Export" button located above the Result Grid.
   - In the "Export Data" dialog, select "CSV" as the format.
   - Choose a location to save the CSV file, name it `departments.csv`, and click "Save".

3. **Export `dept_emp` Table:**
   - Execute the SELECT statement for the `dept_emp` table.
   - Click on the "Export" button located above the Result Grid.
   - In the "Export Data" dialog, select "CSV" as the format.
   - Choose a location to save the CSV file, name it `dept_emp.csv`, and click "Save".
### Now that we have CSV files let's connect to them using Tableau

### Summary

- **Columns:** `emp no`
- **Rows:** `dept name`
- **Label:** `emp no`
- **Filter:** `dept name`


1. **Open Tableau and Connect to Your Data:**
   - Open Tableau and connect to the CSV files (`employees`, `departments`, and `dept_emp`). In many cases when you connect to the first CSV file let's say `employees.csv` Tableau will connect to the rest too but if not then you need to connect to all of them on by one.

<img src="/part-3/pics/rev-1.png" width="500" />


2. **Join the Data:**
   - Go to the Data Source tab.
   - Drag the `employees` CSV to the canvas.
   - Drag the `dept_emp` CSV to the canvas and join it with `employees` on the `emp no` field.
   - Drag the `departments` CSV to the canvas and join it with `dept_emp` on the `dept no` field.

<img src="/part-3/pics/rev-2.png" width="500" />

3. **Create a New Worksheet:[Optional]**
   - Click on the "Sheet 1" tab at the bottom to create a new worksheet.

4. **Add 'emp no' to Columns:**
   - In the Data pane, find the `emp no` field (from the `employees` table).
   - Drag `emp no` to the Columns shelf.

5. **Add 'dept name' to Rows:**
   - In the Data pane, find the `dept name` field (from the `departments` table).
   - Drag `dept name` to the Rows shelf.

6. **Add 'emp no' to Labels:**
   - In the Data pane, find the `emp no` field again.
   - Drag `emp no` to the Label shelf in the Marks card.

7. **Add 'dept name' as a Filter:**
   - In the Data pane, find the `dept name` field.
   - Drag `dept name` to the Filters shelf.
   - A filter dialog will appear. Select the departments you want to include in the filter and click OK.

8. **Adjust the Bar Chart:**
   - Ensure that the Marks card is set to "Bar".
   - You can adjust the size, color, and other properties of the bars as needed.

9. **Customize Labels:**
   - Click on the Label shelf in the Marks card.
   - Ensure that "Show mark labels" is checked.
   - You can customize the font, size, and alignment of the labels as needed.

<img src="/part-3/pics/rev-2.png" width="500" />


10. **Save Your Worksheet:**
    - Save your worksheet by clicking on "File" >  "Save" or "Save As" and choose a location to save your Tableau workbook.


# Pie Chart now

Certainly! Here are the revised instructions for creating a Pie Chart in Tableau, assuming you are already connected to your data and have joined the tables:

### Summary

- **Columns:** `emp no`
- **Filters:** `Dept Name`
- **Rows:** `gender`
- **Marks Card:**
  - **Type:** Pie
  - **Color:** `gender`
  - **Angle:** `emp no`
  - **Label:** `gender`
  - **Label:** `emp no`
  - **Size:** `emp no`

Step-by-Step Instructions

1. **Create a New Worksheet:**
   - Click on the "New Woksheet" button right next to your current worksheet tab at the bottom to create a new worksheet.

2. **Add 'emp no' to Columns:**
   - In the Data pane, find the `emp no` field (from the `employees` table).
   - Drag `emp no` to the Columns shelf.

3. **Add 'gender' to Rows:**
   - In the Data pane, find the `gender` field (from the `employees` table).
   - Drag `gender` to the Rows shelf.

4. **Convert to Pie Chart:**
   - In the Marks card, click on the drop-down menu and select "Pie". Your chart will initially resemble the one in the following picture, but we will refine it shortly.

<img src="/part-3/pics/rev-3.png" width="500" />


5. **Add 'gender' to Color & Label:**
   - In the Data pane, find the `gender` field again.
   - Drag `gender` to the Color shelf in the Marks card.
   - Drag `gender` to the Label shelf in the Marks card.

6. **Convert it to Pie Chart:**
   - Click on `Show Me` and pick Pie Chart.
   - This will automatically configure your settings, resulting in a well-presented pie chart.

<img src="/part-3/pics/rev-4.png" width="500" />  


7. **Adjust the Pie Chart:**
   - Click on the Size shelf in the Marks card to adjust the size of the pie chart.
   - You can also adjust the colors by clicking on the Color shelf and selecting the desired colors for each gender.

8. **Customize Labels:**
   - Click on the Label shelf in the Marks card.
   - Ensure that "Show mark labels" is checked.
   - You can customize the font, size, and alignment of the labels as needed.

9. **Save Your Worksheet:**
   - Save your worksheet by clicking on "File" >  "Save" or "Save As" and choose a location to save your Tableau workbook.













.
.

<img src="/part-3/pics/rev-1.png" width="500" />

.
.
