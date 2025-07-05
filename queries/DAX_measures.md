# DAX Measures Used in Power BI Dashboard

#### Average Salary
```DAX
Average Salary
Average Salary =AVERAGE('Palmoria Group emp-data'[Total Salary])

Salary Pay Gap
Salary Pay Gap = MAX([Total Salary]) - MIN(Total[Salary])

Compliance calcations
indication of employee that was paid 90,000 above = IF([Total_Salary]>=90000,"1","0")
Count of compliance = (CALCULATE( COUNTROWS(FILTER('Palmoria employee data','Palmoria employee data'[Total_Salary]>=90000))))
Compliance percentage  (%) = [total compliance]/[Total Employee]
 

Total Employee
Total Employee = DistinctCOUNT('Palmoria Group emp-data'[Name])
