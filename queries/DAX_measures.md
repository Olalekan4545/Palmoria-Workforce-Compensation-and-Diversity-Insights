# DAX Measures Used in Power BI Dashboard

#### Average Salary
```DAX
Average Salary
Average Salary =AVERAGE('Palmoria Group emp-data'[Total Salary])

Salary Pay Gap
Salary Pay Gap = MAX([Total Salary]) - MIN(Total[Salary])

Compliance Rate
Compliance Rate (%) =
 Compliance Rate = ( COUNTROWS(FILTER('Palmoria Group emp-data','Palmoria Group emp-data'[Total Salary]>=90000))/'Palmoria Group emp-data'[Total Employee])

Total Employee
Total Employee = COUNT('Palmoria Group emp-data'[Name])
