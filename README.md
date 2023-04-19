# AMEO-Dataset-EDA-VISUALIZATION
### 1) What is EDA❓
EDA stands for Exploratory Data Analysis, which is an approach to analyzing and understanding data. EDA is a critical step in data analysis that involves examining and summarizing data to gain insights and identify patterns, relationships, and anomalies in the data.

EDA typically involves visualizing the data using various graphs and charts, such as histograms, box plots scatter plots, and heat maps etc to understand the distribution, range, and relationships between variables. It also involves performing summary statistics like mean, median, mode, standard deviation, correlation coefficients, and percentiles to provide a quantitative summary of the data.

EDA is useful in data analysis because it can help identify potential data quality issues, outliers, and missing data. It can also help in identifying potential relationships between variables, which can guide the development of predictive models or inform decision-making. Additionally, EDA can help in identifying biases and assumptions in the data, which can be important in certain contexts, such as in social science or health research.

### 2) What is AMEO Dataset❓
The dataset was released by Aspiring Minds from the Aspiring Mind Employment Outcome 2015 (AMEO). The study is primarily limited  only to students with engineering disciplines. The dataset contains the employment outcomes of engineering graduates as dependent variables (Salary, Job Titles, and Job Locations) along with the standardized scores from three different areas – cognitive skills, technical skills and personality skills. The dataset also contains demographic features. The dataset  contains  around  40 independent variables and 4000 data points. The independent variables are both continuous and categorical in nature. The dataset contains a unique identifier for each candidate. Below mentioned table contains the details for the original dataset.  

## 3) The Dataset Content
| VARIABLES              | TYPE           | Description                                               |
|------------------------|------------------|-----------------------------------------------------------|
| ID                     | UID             | A unique ID to identify a candidate                      |
| Salary                 | Continuous      | Annual CTC oﬀered to the candidate (in INR)               |
| DOJ                    | Date            | Date of joining the company                               |
| DOL                    | Date            | Date of leaving the company                               |
| Designation            | Categorical     | Designation oﬀered in the job                             |
| JobCity                | Categorical     | Location of the job (city)                                |
| Gender                 | Categorical     | Candidate’s gender                                        |
| DOB                    | Date            | Date of birth of candidate                                |
| 10percentage           | Continuous      | Overall marks obtained in grade 10 examinations           |
| 10board                | Continuous      | The school board whose curriculum the candidate followed in grade 10 |
| 12graduation           | Date            | Year of graduation - senior year high school              |
| 12percentage           | Continuous      | Overall marks obtained in grade 12 examinations           |
| 12board                | Date            | The school board whose curriculum the candidate followed in grade 12 |
| CollegeID              | NA/ID           | Unique ID identifying the college which the candidate attended |
| CollegeTier            | Categorical     | Tier of college                                           |
| Degree                 | Categorical     | Degree obtained/pursued by the candidate                  |
| Specialization         | Categorical     | Specialization pursued by the candidate                   |
| CollegeGPA             | Continuous      | Aggregate GPA at graduation                              |
| CollegeCityID          | NA/ID           | A unique ID to identify the city in which the college is located in |
| CollegeCityTier        | Categorical     | The tier of the city in which the college is located      |
| CollegeState           | Categorical     | Name of States                                            |
| GraduationYear         | Date            | Year of graduation (Bachelor’s degree)                     |
| English                | Continuous      | Scores in AMCAT English section                           |
| Logical                | Continuous      | Scores in AMCAT Logical section                           |
| Quant                  | Continuous      | Scores in AMCAT Quantitative section                      |
| Domain                 | Continuous/Standardized | Scores in AMCAT’s domain module                      |
| ComputerProgramming    | Continuous      | Score in AMCAT’s Computer programming section             |
| ElectronicsAndSemicon  | Continuous      | Score in AMCAT’s Electronics & Semiconductor Engineering section |
| ComputerScience        | Continuous      | Score in AMCAT’s Computer Science section                 |
| MechanicalEngg         | Continuous      | Score in AMCAT’s Mechanical Engineering section           |
| ElectricalEngg         | Continuous      | Score in AMCAT’s Electrical Engineering section           |
| TelecomEngg            | Continuous      | Score in AMCAT’s Telecommunication Engineering section    |
| CivilEngg              | Continuous      | Score in AMCAT’s Civil Engineering section                |
| conscientiousness      | Continuous/Standardized | Scores in one of the sections of AMCAT’s personality test |
| agreeableness          | Continuous/Standardized | Scores in one of the sections of AMCAT’s personality test |
| extraversion           | Continuous/Standardized | Scores in one of the sections of AMCAT’s personality test |
| neuroticism            | Continuous/Standardized | Scores in one of the sections of AMCAT’s personality test |
| openness_to_experience | Continuous/Standardized | Scores in one of the sections of AMCAT’s personality test |

### Some Research Question I am working with
> **Times of India article dated Jan 18, 2019 states that “After doing your Computer Science Engineering if you take up jobs as a Programming Analyst, Software Engineer, Hardware Engineer and Associate Engineer you can earn up to 2.5-3 lakhs as a fresh graduate.” Test this claim with the data given to you.**

`sal_df = ch.groupby(["Designation", "Specialization"])["Salary"].mean()`

**The output is -**
1. associate engineer  CSE               245000.000000
2. programmer analyst  CSE               346951.219512
3. software engineer   CSE               348032.581454

`if ((cs.Salary >= 250000) & (cs.Salary <= 300000)).all():
    print("The Claim of TOI is True")
 else:
    print("The Claim of TOI is Not True")`
   
**The output is -**
The Claim of TOI is Not True

## Also there are so many research questions and observations, please visit the jupyter notebook file 😊
