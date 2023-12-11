# Context
In any organization, the crucial factor for success lies in the ability to attract and retain top-tier talent. As an HR analyst in my company, one of my responsibilities involves identifying the factors that influence employees to stay or leave. The goal is to pinpoint the aspects that can be modified to prevent the departure of valuable personnel, with the aid of Watson Analytics.

## Problem
Based on the data, 16.1% of employees have opted to leave, while the remaining 83.9% have chosen to stay. This situation, if left unaddressed, may result in excessive costs.

## Data Description
The dataset comprises:
- 35 columns
- 1470 rows

## Analysis
Insights gleaned from the analysis are as follows:

- In terms of sheer numbers, male employees are more likely to leave, with a slight difference of just over 2% compared to their female counterparts.
- While the R&D department has a higher overall exit count, the proportion of departures is higher in the Sales department.
- Further examination reveals that within the Sales department, Sales Representatives are the most likely to leave, whereas in R&D, it is Laboratory Technicians.
- The average commuting distance to the office appears to influence the decision to leave the company.
- Employees who leave have an average tenure of over 5 years.
- The highest number of departures occurs within the first 5 years of employment, with a significant number leaving within the first year.
- The distance from home varies among employees who decide to leave, with the majority residing 1-2 kilometers away.
- Job satisfaction plays a role, as lower ratings correspond to a higher likelihood of employees leaving.
- Those who rate their environmentsatisfaction as 1 are more inclined to resign.
- Employees with additional working hours or overtime are more likely to resign, indicating an impact on work-life balance.
- Employees with the lowest job involvement level (1) are more prone to leaving, accounting for approximately 33.27% of departures.
- Lower-level employees are more likely to leave, potentially due to attractive offers from other companies and a desire for career advancement.
- Employees with salaries below $4200 are more likely to resign.

## Modeling & Prediction
In this stage, the evaluation metric used is "Recall," prioritizing the minimization of false negatives. This is crucial to identify employees predicted as not leaving but who actually intend to do so. The aim is to provide targeted interventions for those predicted to leave.

### Models Used
- k-Nearest Neighbor
- Decision Tree
- RandomForest
- AdaBoost
- XGBoost

In assessing the performance of the five employed models, we conducted a comparison of the recall metric before and after hyperparameter tuning.
![image](https://github.com/ridhoditya/T3chS3nse/assets/139097412/eac22093-817c-44e2-81d0-b76c352b7ebc)

![image](https://github.com/ridhoditya/T3chS3nse/assets/139097412/a6d593f6-7d08-4b87-94fb-9830274a3bbe)

### Features Importance
After careful consideration, the decision has been made that the most optimal model is Adaboost, with the following features being identified as crucial:
![image](https://github.com/ridhoditya/T3chS3nse/assets/139097412/3d224e72-8dd1-4c87-9a6f-d9c74ad0f901)


### Evaluation Metric
![image](https://github.com/ridhoditya/T3chS3nse/assets/139097412/5b5428c7-5f9e-44d4-a1d7-4ed55f9d5196)

##Business Simulation
A decrease in the attrition rate has been observed.
![image](https://github.com/ridhoditya/T3chS3nse/assets/139097412/cda8f93b-f70d-40c5-9f0a-6d3ffdab3128)




# Business Recommendations
1. Implement Regular Performance Appraisals: Conduct routine performance evaluations to assess employee performance regularly, typically on an annual basis. This practice helps understand the extent to which employees have achieved their goals and provides feedback for improvement.

2. Reward High-Performing and Loyal Employees: Recognize and reward employees who demonstrate outstanding performance and loyalty to the company through bonuses or incentives.

3. Reduce Overtime Hours: Minimize overtime to decrease the likelihood of employee turnover, promoting a better work-life balance and satisfaction.

4. Re-evaluate Workload: Regularly assess employee workloads to ensure tasks align with their capacity, preventing excessive stress and fatigue.

5. Provide Relevant Training and Development: Offer appropriate training and development opportunities to enhance employee skills, demonstrating appreciation and improving their work quality.

6. Consider Employee Wellness Programs: Implement wellness initiatives, including health programs, psychological support, and stress management, to enhance employee well-being and productivity.

  All these practices are crucial for fostering a healthy work environment, motivating employees, and minimizing turnover. Consequently, organizations can achieve improved performance and remain competitive in the market.







