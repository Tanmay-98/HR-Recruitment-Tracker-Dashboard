# Data Dictionary - HR Recruitment Tracker

This data dictionary provides detailed information about the dataset used in the HR Recruitment Tracker project. It includes data types, descriptions, and potential values for each column.

---

## 📦 **1. HR Recruitment Data Table**

| **Column Name**     | **Data Type** | **Description**                           | **Sample Values**       |
|---------------------|---------------|-----------------------------------------|-------------------------|
| candidate_name      | Text         | Name of the candidate                    | John Doe, Jane Smith    |
| job_title           | Text         | Job role applied for                     | Data Analyst, HR Manager |
| cv_date             | Date         | Date the candidate submitted the CV      | 2023-01-15, 2023-02-20  |
| source_of_cv        | Text         | Source through which the CV was received | LinkedIn, Indeed        |
| recruiter           | Text         | Name of the recruiter handling the candidate | Michael Johnson         |
| selection_date      | Date         | Date the candidate was selected          | 2023-01-25, 2023-03-12  |
| first_round_date    | Date         | Date of the first interview round        | 2023-01-18, 2023-02-22  |
| first_round_status  | Text         | Status of the first interview round      | Passed, Rejected        |
| first_round_reason  | Text         | Reason for rejection in the first round  | Incomplete Resume, Lack of Experience |
| second_round_date   | Date         | Date of the second interview round       | 2023-01-21, 2023-02-25  |
| second_round_status | Text         | Status of the second interview round     | Passed, Rejected        |
| final_round_date    | Date         | Date of the final interview round        | 2023-01-23, 2023-02-28  |
| final_round_status  | Text         | Final status of the candidate            | Hired, Rejected         |
| drop_off_stage      | Text         | Stage where the candidate dropped off    | First Round, Second Round, Final Round |

---

## 📅 **2. Date Dimension Table**

| **Column Name** | **Data Type** | **Description**                    | **Sample Values**   |
|-----------------|---------------|------------------------------------|---------------------|
| date            | Date         | Actual date value                   | 2023-01-01          |
| day             | Integer      | Day of the month (1-31)             | 1, 15, 30           |
| month           | Integer      | Month of the year (1-12)            | 1, 2, 12            |
| month_name      | Text         | Full name of the month              | January, February   |
| quarter         | Integer      | Quarter of the year (1-4)           | 1, 2, 3, 4          |
| year            | Integer      | Year                               | 2023, 2024          |
| fiscal_year     | Text         | Fiscal year                        | FY2023, FY2024      |
| day_of_week     | Text         | Day name (Monday-Sunday)           | Monday, Tuesday     |
| is_weekend      | Boolean      | Whether the day is a weekend       | TRUE, FALSE         |

---

## 🎯 **3. Calculated Columns and Measures**

| **Column Name**       | **Data Type** | **Description**                             | **Formula/Calculation**           |
|-----------------------|---------------|-------------------------------------------|----------------------------------|
| total_candidates      | Integer      | Total number of candidates applied         | `COUNTROWS('HR Recruitment')`    |
| total_selected        | Integer      | Total number of candidates selected        | `COUNTROWS(FILTER('HR Recruitment', [final_round_status] = "Hired"))` |
| selection_rate        | Decimal      | Selection rate as a percentage             | `(total_selected / total_candidates) * 100` |
| drop_off_rate         | Decimal      | Drop-off rate at each stage                | `COUNTROWS(FILTER('HR Recruitment', [drop_off_stage] <> "None")) / total_candidates` |
| avg_time_to_hire      | Integer      | Average number of days from CV submission to selection | `AVERAGEX('HR Recruitment', DATEDIFF([cv_date], [selection_date], DAY))` |

---

## 🔥 **4. Potential Issues and Data Quality Considerations**

- **Missing Values:** Ensure that all date columns are filled to prevent calculation errors.
- **Data Inconsistencies:** Verify the format of dates (e.g., YYYY-MM-DD).
- **Data Validation:** Ensure that job titles are consistent and standardized (e.g., 'HR Manager' vs. 'Human Resources Manager').
- **Drop-off Stage Calculation:** Verify that the drop-off stage is correctly marked for candidates who did not proceed to the next round.

---

## 📦 **5. Data Sources and Connections**

- **HRData.xlsx:** Source data for recruitment analysis.
- **Power BI Desktop:** Used for data modeling, transformations, and visualization.

---
