# Connect to CSV files In Tableau

In this blog, we will explore how to export data from MySQL as CSV files and create interactive visualizations in Tableau. We will build a bar chart and a pie chart, combine them into a dashboard with a `dept name` filter, and enable interactivity to dynamically filter the bar chart using the pie chart.


## Agenda

### Data Preparation
1. Exported CSV files from MySQL database.

### Tableau Visualizations
1. Created a bar chart with `emp no`, `dept name`, and filters.
2. Created a pie chart with `emp no`, `gender`, colors, and angles.

### Dashboard Creation
1. Added a vertical container to the dashboard.
2. Placed bar chart and pie chart side by side.
3. Added `dept name` drop-down filter.
4. Applied filter to both charts.

### Interactivity
1. Enabled "Use as Filter" for pie chart.
2. Tested interactivity by filtering bar chart.

### Saving and Exporting
1. Saved Tableau workbook.

##### Let's Get Started


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

# Time to Connect to  CSV files and creating a Bar chart 


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


# Creating a Pie Chart

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




# Creating A Dashboard

Step-by-step instructions to create a dashboard in Tableau, placing the bar chart and pie chart side by side (vertically) using a vertical container, and adding 'dept name' as a filter with a drop-down list:


1. **Create a New Dashboard:**
   - Click on the "New Dashboard" button at the bottom of Tableau.

2. **Set Up the Dashboard Layout:**
   - In the Dashboard pane on the left, ensure that "Show Dashboard Title" is checked if you want to display a title.
   - Drag a "Vertical" layout container from the Objects section to the dashboard workspace.

3. **Add Sheets to the Vertical Container:**
   - Drag "Sheet 1" (the bar chart) from the Sheets section to the vertical container.
   - Drag "Sheet 2" (the pie chart) from the Sheets section to the vertical container, placing it below "Sheet 1".

Remove any filters or color options from all the charts, so only the bar and pie charts are visible side by side. Drag a 'Vertical Container' from 'Objects' and place it above both charts.

<img src="/part-3/pics/zz-5.png" width="500" />

4. **Add 'dept name' as a Filter:**
Now, click on the 'More Options' drop-down arrow on either chart, go to 'Filter', and select 'Dept Name'. If this does not automatically add the filter to the empty container we created, you can manually drag and drop it into the container. Then, change its options to 'Single Value (dropdown)'.

<img src="/part-3/pics/zz-4.png" width="500" />

6. **Apply the Filter to Both Sheets:**
   - Click on the drop-down arrow on the `dept name` filter card again.
   - Select "Apply to Worksheets" > "Selected Worksheets".
   - In the dialog that appears, check both "Sheet 1" and "Sheet 2" to apply the filter to both charts.
   - Click OK.

7. **Adjust the Layout and Appearance:**
   - Resize the charts and the filter card as needed to ensure a clean and organized layout.
   - You can adjust the size of the vertical container by clicking and dragging its borders.

8. **Save Your Dashboard:**
   - Save your dashboard by clicking on "File" > "Save" or  "Save As" and choose a location to save your Tableau workbook.


# Interactive Charts

To make the pie chart interactive on this dashboard, you can use the "Filter" action in Tableau. Here are the step-by-step instructions:

#### Method: 1

Step-by-Step Instructions

1. **Select the Pie Chart:**
   - Click on the pie chart ("Sheet 2") to select it.

2. **Enable "Use as Filter":**
   - In the top-right corner of the pie chart, click on the drop-down arrow (more options).
   - Select "Use as Filter" from the drop-down menu.

<img src="/part-3/pics/zz-6.png" width="500" />

<img src="/part-3/pics/zz-7.png" width="500" />

3. **Test the Interactivity:**
   - In the dashboard workspace, click on a specific slice of the pie chart.
   - The bar chart should now filter and display data only for the selected slice (department).



#### Method: 2

1. **Select the Pie Chart:**
   - In the dashboard workspace, click on the pie chart ("Sheet 2") to select it.

2. **Open the Actions Menu:**
   - In the top menu, go to "Worksheet" > "Actions".

3. **Create a New Filter Action:**
   - In the Actions dialog box, click on the "Add Action" button.
   - From the list of actions, select "Filter".

4. **Configure the Filter Action:**
   - In the "Source Sheets" section, ensure that "Sheet 2" (the pie chart) is selected.
   - In the "Target Sheets" section, check the box for "Sheet 1" (the bar chart).
   - In the "Clearing the selection" check "show all values"
Leave everthing else default.

7. **Save the Action:**
   - Click "OK" to save the filter action.

8. **Test the Interactivity:**
   - In the dashboard workspace, hover over a slice of the pie chart.
   - Click on a specific department slice.
   - The bar chart should now filter and display data only for the selected department.
<img src="/part-3/pics/zz-7.png" width="500" />

<img src="/part-3/pics/zz-8.png" width="500" />

10. **Save Your Dashboard:**
    - Save your dashboard by clicking on "File" > "Save" or "Save As" and choose a location to save your Tableau workbook.





.
.



.
.
