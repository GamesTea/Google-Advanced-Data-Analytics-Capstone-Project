# Logistic Regression, Decision Tree and Random Forest Analysis of Employee Satisfaction

There is a high rate of turnover among Salifort employees (a fictional company). Salifort’s senior leadership team is concerned about how many employees are leaving the company. Salifort strives to create a corporate culture that supports employee success and professional development. Further, the high turnover rate is costly in the financial sense. Salifort makes a big investment in recruiting, training, and upskilling its employees. If Salifort could predict whether an employee will leave the company, and discover the reasons behind their departure, they could better understand the problem and develop a solution. 

As a first step, the leadership team asks Human Resources to survey a sample of employees to learn more about what might be driving turnover.  

Next, the leadership team asks you to analyze the survey data and come up with ideas for how to increase employee retention. To help with this, they suggest you design a model that predicts whether an employee will leave the company based on their job title, department, number of projects, average monthly hours, and any other relevant data points. A good model will help the company increase retention and job satisfaction for current employees, and save money and time training new employees. 

## Project Overview

Since the variable we are seeking to predict is categorical (whether an emplooye is likely to leave or not), the models that could that could be built for this task are either a Linear Regression or a tree-based machine learning model. In this project, both approaches were taken and compared in their efficacy.
While the linear regression model performed adequately and with speed (with an overall accuracy of 82%), it had more trouble predicting employees who do leave when it predicted they would not (a false negative result).
![image](https://github.com/user-attachments/assets/37f96785-a741-4069-bc15-62b56028b8f0)
![image](https://github.com/user-attachments/assets/272370b9-c09d-46ff-84bd-24dca01dfa3c)

The tree-based approach, on the other hand, while taking longer to process, was able to achieve much higher accuracy and lower the instances of false negatives/positives, a basic decision tree managed to achieve a higher overall scoring than the Linear Regression model.
![image](https://github.com/user-attachments/assets/0d1696aa-7a9d-4f41-b856-ecdd0e474337)

However, because these models are prone to over-fitting, a Random Forest was then used. Bearing in mind that these models take much longer to process than lone Decision Trees, applying them to larger datasets, or even incorporating broader hyperparameters will increase their processing times immensely. Despite this, a Random Forest model is capable of achieving better scoring metrics and better predict on data it has never seen before.

![image](https://github.com/user-attachments/assets/29904fc0-8911-46ec-bb51-8253f8cba151)


## Business Understanding 

These models help predict whether an employee will leave and identify which factors are most influential. These insights can help HR make decisions to improve employee retention.
Several key factors became apparent on whether or not an employee would leave the company, such as the number of projects they are working on, their work hours (indicating whether or not they are working overtime), how well their last evaluation went and how long they have been working at the company.
![image](https://github.com/user-attachments/assets/f254631a-ac95-40d0-b739-5eaf7fff1a99)

### Insights/Next Steps


## Data Understanding 

The dataset used for this project contains 14,999 rows – each row is a different employee’s self-reported information

10 Rows

![image](https://github.com/user-attachments/assets/9a9cf0b4-7f87-4cb8-acc6-dda781555b76)

While no data was missing from this dataset, there were 3008 rows of duplicated data that had to be removed before modeling could beging.
Beyond that, several outliers were found in the tenure column, which had to be removed as well.
![image](https://github.com/user-attachments/assets/7a841079-ebc4-4a11-a627-eb1da1ea066c)


## Conclusion
We came to the conclusion that a lot of employees were leaving due to having too many projects to work in, long hours and not seeing this effort reflected in terms of promotions and compensation. Beyond that there was a discrepancy in employees receiving higher reviews for working in more projects and working long hours, which possibly fosters an environment that does not encourage a healthy work/life balance. As such the following recomendations are made based off the data observed:

- Cap the number of projects that employees can work on.
- Consider promoting employees who have been with the company for at least four years, or conduct further investigation about why four-year tenured employees are so dissatisfied.
- Either reward employees for working longer hours, or don't require them to do so.
- If employees aren't familiar with the company's overtime pay policies, inform them about this. If the expectations around workload and time off aren't explicit, make them clear.
- Hold company-wide and within-team discussions to understand and address the company work culture, across the board and in specific contexts.
- High evaluation scores should not be reserved for employees who work 200+ hours per month. Consider a proportionate scale for rewarding employees who contribute more/put in more effort.
