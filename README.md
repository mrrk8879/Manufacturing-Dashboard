# Manufacturing Data Analysis - Power BI Dashboard

## Project Overview
This project involves the creation of comprehensive Power BI dashboards to analyze manufacturing and employee data. The dashboards provide insights into production metrics, employee performance, and operational efficiency across different countries, departments, and product types.

## Datasets
The analysis is based on two primary datasets:

### 1. Employee Dataset
Contains information about employees with the following columns:
- **EmployeeID**: Primary key
- **Department**: Sale (166), Quality Control (153), Human Resource (158), Production (151), Logistics (155)
- **HireDate**: Date of employee hiring
- **Salary**: Employee compensation (Float)
- **Country**: India (151), China (155), Japan (157), USA (176), Germany (161)
- **ProductID**: Foreign key to the Production table
- **Performance Rating**: Scale of 1-10
- **Employee Training**: Training information (Text)

### 2. Production Dataset
Contains information about manufacturing operations:
- **ProductID**: Primary key
- **Product Type**: Automobiles, Electronics, Furniture, Machinery, Textile
- **ProductionDate**: Date of production
- **Production Cost**: Cost of production (Float)
- **Country**: India, China, Japan, Germany, USA
- **QuantityProduced**: Units produced (Integer)
- **Warehouse Location**: North, West, South, East

## Data Cleaning & Preprocessing
The following data cleaning steps were performed:
- Removed missing and inconsistent values from Department and Warehouse Location fields
- Imputed median values for missing entries in Salary, Performance Rating, Production Cost, and Quantity Produced
- Converted timestamp data to proper date format
- Adjusted data types as needed for analysis

## Feature Engineering
Several derived columns were created to enhance analysis:
- **SubProduct Type**: Categorized products based on production cost into High, Mid, and Low (using 33.33 and 66.66 percentiles)
- **Salary Category**: Classified employees based on salary into High, Mid, and Low (using 33.33 and 66.66 percentiles)
- **Tenure**: Calculated employment duration from hire date to the latest production date
- **Training Lists**: Created columns to store training dates and types

## Dashboards

### Employee Dashboard
https://drive.google.com/file/d/105LV0ycyxHVCJ7toeASrmDSRTKdQCxMq/view?usp=drive_link

**Key Metrics:**
- Total Employees: 775
- Average Performance Rating: 4.91/10
- Average Salary: $55.13K

**Visualizations:**
1. **Time Series Analysis**: Line chart showing salary trends over time by department
2. **Department Distribution**: Column chart comparing employee count across departments
   - Sales department has the highest number (165 employees)
   - HR follows with 155 employees
3. **Training Distribution**: Donut chart showing the proportion of employees by number of trainings taken
   - 33.94% of employees have taken 1 training
   - 33.68% have taken 3 trainings
4. **Performance Analysis**: Decomposition tree for root cause analysis of performance ratings
   - Conditional formatting: 0-5 (Red), 5-7 (Light Green), 7+ (Green)
   - Layered by department, country, salary category, and training count
5. **Geographic Distribution**: Treemap showing employee distribution by country
   - USA has the highest employee count
   - Medium-salary employees are most prevalent in the USA

**Interactive Elements:**
- Date slicer for filtering by hire date
- Advanced slicers for country, department, and product filters

### Production Dashboard
https://drive.google.com/file/d/104r8jmolG3gjs6hTgkTlJ550hjc78Rzc/view?usp=sharing

**Key Metrics:**
- Total Quantity Produced: 538K units
- Average Production: 10.34K units

**Visualizations:**
1. **Production Cost Analysis**: Line chart comparing average production costs by product type
   - Automobiles have the highest average production cost
   - Textiles follow as the second highest
2. **Geographic Cost Analysis**: Treemap comparing production costs by country
   - USA has the highest production costs
   - India follows as the second highest
3. **Production Distribution**: Donut charts showing:
   - Proportion of quantity produced by product type (Textile leads, followed by Automobiles)
   - Proportion of quantity produced by country (Germany produces the most, followed by Japan)
4. **Cost Efficiency Analysis**: Column charts showing:
   - Cost efficiency by product type
   - Cost efficiency by country for each product type
   - Textiles have the lowest per-unit production cost
   - German textile production is most cost-efficient
   - Automobile production is most expensive per unit, with China having the highest cost ($22 per unit)
5. **Production Trends**: Line chart showing quantity produced over time
   - Lowest production: Electronics in October (3,616 units)
   - Highest production: Electronics in September (15,450 units)

**Interactive Elements:**
- Date slicer for filtering by production date
- Advanced slicers for country, quantity category, and product filters
- Page navigation icons for switching between dashboards
- "Clear All" slicer button for resetting filters

## Key Insights

### Employee Insights
- Sales department has the largest workforce
- Average performance rating is relatively low at 4.91/10
- USA has the highest number of employees, with most in the medium salary range
- One-third of employees have only taken a single training

### Production Insights
- Textiles and Automobiles are the most produced product types
- Germany and Japan lead in production quantity
- Automobiles have the highest production cost overall
- Textiles have the lowest per-unit production cost
- USA has the highest production costs across product categories
- Electronics production showed the highest variance, with both the lowest and highest monthly production quantities

## Navigation and Usability
The dashboard includes:
- Interactive navigation between Employee and Production views
- Multiple filtering options for detailed analysis
- Clear visualization formatting for easy interpretation
- Conditional formatting to highlight performance thresholds

## Future Work
Potential enhancements for future iterations:
- Predictive analytics for production planning
- Employee retention analysis
- Cost optimization modeling
- Seasonal trend analysis for production fluctuations

## Tools Used
- Power BI Desktop
- Excel (for initial data preprocessing)

## Author
Team leader - Mohd Rihan Khan
Member 1 - Mokhit Pathan
Member 2 - Sanjay Dalawai
Member 3 - Yogesh Kumar Saini
Member 4 - Abhijit Kumar

## Last Updated
February 27, 2025
