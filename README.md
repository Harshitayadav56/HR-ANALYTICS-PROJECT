# HR-ANALYTICS- PROJECT  

## ATLIQ HARDWARE PRESENCE INSIGHT DASHBOARD


This project involved the use of Power Query and DAX Query to analyze employee attendance data in real-time, adding new measures and columns, and creating a Power BI Dashboard. The goal is to deliver insights into attendance patterns and identify areas for improvement for HR.
###

## Tools used
1. Power BI
2. Power Query
3. Dax Query
4. Data modeling
###

## Cleaning and Analyzing Data using Power Query
1. Open Excel and connect to the data provided
2. Then combine data from multiple sheets and column in excel to  Power BI
2. Then transform data in Power Query Editor to clean and analyze the data
3. Create a copy template for one sheet in Power Query transformations and apply the same transformations to all sheets
4. Perform all necessary cleaning steps, such as removing duplicates, renaming columns, changing data types, pivot or unpivot the columns
5. Create a parameter to select the desired data based on a specific condition
6. Encapsulate all steps into a function to be reused for future sheets and data
7. Load and Apply the cleaned data into Power BI
###

## Using DAX Query
1. Total working days = 
Var totaldays= COUNT('Final data'[Value])
Var nonworkdays= CALCULATE (COUNT('Final data'[Value],'Final data'[value] in {"WO" , "HO"})
RETURN
totaldays - nonworkdays

2. Present Days = 
Var Presentdays = CALCULATE(COUNT('Final data'[Value],'Final data'[value]="P")
RETURN
Presentdays + [WFH Count]

3. WFH Count = SWITCH(TRUE()
'Final data'[value] = "WFH' , 1,
'Final data'[value] = "HWFH" , 0.5,
0)

4. SL Count = SUM('Final data'[SL Count])


5. Presence % = DIVIDE([Present days],'Measure table'[Total working days],0)

6. WFH % = DIVIDE([WFH Count], [Present days],0)

7. SL % = DIVIDE([SL Count], [Present days],0)
###



## Power BI Dashboard Visualization
1. Design the dashboard layout
2. Add all the charts required from visualization - build visual tool
2. Use Visulization - format visual for editing the charts
3. Add the most important insight on the top left side of the dashboard
4. Add the Title
5. Add Month column as Slicer and add some informative KPI.
6. Now, give the attractive look to the dashboard so that it looks presentable to the stakeholders.
###

## Key Takeaways
1. Gained experience in telling data driven stories through a well designed dashboard
2. Learned to create matrices and measures using DAX
3. Developed analytical and visualization skills
4. Improved ability to select the appropriate chart types for effective visualization
5. Developed a deeper understanding of HR processes and requirements
6. Copy Paste visuals and alter them to boost the productivity.
