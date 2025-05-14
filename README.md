# HR Recruitment Tracker

## 📦 Project Overview

The HR Recruitment Tracker is a comprehensive Power BI project developed to analyze and monitor the recruitment performance of a large retail organization over a span of three years. This project leverages data modeling, interactive visualizations, and key performance indicators (KPIs) to provide insightful analysis on recruitment trends, candidate selection rates, and recruiter performance.

## 📁 Dataset

The dataset comprises two tables:
- **HR Recruitment Data:** Includes candidate information, job roles, interview rounds, and selection statuses.
- **Date Dimension Table:** Custom table created for time-based analysis and managing data relationships effectively.

### Key Columns in HR Recruitment Data:
- Candidate Name
- Job Title
- CV Date
- Source of CV
- Recruiter
- Selection Date
- Interview Round Dates & Statuses
- Reasons for Rejection

### Date Dimension Table:
- Date
- Year
- Quarter
- Month
- Week
- Day of Week
- Fiscal Year

## ✅ Objectives
- Analyze recruitment data to identify trends in candidate sourcing and selection.
- Assess recruiter performance based on hiring success rates.
- Monitor candidate drop-off rates across various interview stages.
- Calculate average time-to-hire and identify recruitment bottlenecks.
- Provide actionable insights for improving recruitment strategies.

## 🛠️ Features and Components

1. **Data Modeling:**
   - Establish relationships between the HR Recruitment Data and Date Dimension Table.
   - Manage active and inactive relationships for in-depth analysis.

2. **Data Transformation:**
   - Cleaning and formatting of data for accuracy and consistency.

3. **KPIs and Measures:**
   - Total Candidates Applied
   - Total Candidates Selected
   - Selection Rate
   - Drop-off Rate by Interview Stage
   - Average Time to Hire

4. **Interactive Visuals:**
   - Line Chart for Candidates Applied per Month
   - Funnel Chart for Interview Stage Drop-off
   - Bar Chart for Job Title-wise Performance
   - Slicer for Year and Recruiter Filtering
   - KPI Cards for Recruitment Metrics

5. **Interactivity and User Experience:**
   - Implemented slicers for filtering data by job role, recruiter, and time period.
   - Navigation buttons for seamless report interaction.
   - Tooltip visuals for enhanced data insights.

## 📊 Insights and Analysis
- Identification of top-performing recruiters based on selection rates.
- Analysis of job roles with the highest and lowest selection rates.
- Trend analysis of recruitment sources to identify effective channels.
- Insights into candidate drop-off stages to improve interview processes.
- Recommendations for optimizing average time-to-hire.

## 📦 How to Run the Project
1. Clone the repository: 
   ```bash
   git clone https://github.com/Tanmay-98/HR-Recruitment-Tracker-Dashboard.git
   ```
2. Open the Power BI file (`HR_Dashboard.pbix`) in Power BI Desktop.
3. Ensure that the `HRData.xlsx` dataset is located in the same directory.
4. Refresh the data and validate the data model.
5. Explore the dashboard and interact with the slicers and buttons.

## ✅ Deliverables
- Power BI Report (`HR_Dashboard.pbix`)
- Dataset (`HRData.xlsx`)
- README file

## 📅 Future Scope
- Implement AI visuals for predictive analysis.
- Incorporate drill-through pages for in-depth recruiter performance analysis.
- Develop a recruitment forecasting model using historical data.

## 🛠️ Technologies Used
- Power BI
- DAX
- Data Modeling
- Data Transformation
- Data Visualization

## 📝 Author
- Tanmay Pathak
