# HR Data Analysis Using Tableau

An interactive Tableau dashboard for exploring employee attrition and workforce characteristics. It brings key HR measures and several demographic, departmental, and job-related views together so that patterns can be explored at a glance and by filtering the data.

## The problem

Employee turnover can affect staffing, continuity, and retention costs. A spreadsheet with employee-level records is difficult to scan for patterns across departments, age groups, education, gender, and job satisfaction. The goal of this project is to make those patterns easier to compare and investigate with an interactive dashboard.

## The solution

The dashboard combines headline measures with linked visualizations:

- **Employee Count**, **Attrition Count**, **Attrition Rate**, **Active Employees**, and **Average Age**
- Attrition counts by department and education field
- Employee counts across age groups
- Job satisfaction ratings by job role
- Gender and age-group comparisons
- An **Education** filter and an age-bin size control
- A department chart action: selecting a department segment filters the other views. The supplied filtered screenshot shows the Sales selection.

With the full dataset, the dashboard shows 1,470 employees, 237 attritions, a 16.12% attrition rate, 1,233 active employees, and an average age of 37. With Sales selected, it shows 446 employees, 92 attritions, a 20.63% attrition rate, 354 active employees, and an average age of 37. These values describe the dataset represented in the screenshots, not current workforce data.

## Dataset

The workbook is `HR Data.xlsx`. It contains one worksheet (`HR data`) with 1,470 employee records and 39 columns (one record per employee). Fields cover:

- Attrition status and derived labels
- Department, job role, business travel, and overtime
- Age, gender, marital status, and education
- Job, environment, and relationship satisfaction and involvement ratings
- Salary and daily/hourly/monthly rates
- Training, performance, company experience, tenure, and promotion history

The workbook includes both source fields and helper/derived columns (for example, age-band and current-employee labels).

## How it was built

The project was created in Tableau using the Excel workbook as its data source:

1. Connected Tableau to `HR Data.xlsx` and select the `HR data` worksheet.
2. Used employee-level records to build the attrition and workforce measures. The dashboard's headline calculations are:
   - **Employee Count**: number of employees
   - **Attrition Count**: employees marked as attrition
   - **Attrition Rate**: attrition count divided by employee count
   - **Active Employees**: employee count minus attrition count
   - **Average Age**: average employee age
3. Created worksheets for departmental and education attrition, age-group counts, job satisfaction by role, and gender/age-group comparisons.
4. Assembled the worksheets into a single dashboard, add the education filter and age-bin control, and configure the department selection to act as a dashboard filter.
5. Checked the overall and filtered views, and successfully extracted useful information by analysis.


## Screenshots

### Full dashboard

![HR Analytics Dashboard — full view](./HR%20Analytics%20Dashboard.png)

### Dashboard with department action filter applied

The view below shows the dashboard after selecting Sales in the department chart.

![HR Analytics Dashboard — Sales department selected](./Action%20Filter%20Applied.png)
