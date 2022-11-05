# (Student Performance in Exams)
## by (Jennifer Ashishali Ochonogor)


## Dataset

This is a fictional dataset sourced from [Kaggle](https://www.kaggle.com/datasets/whenamancodes/students-performance-in-exams?resource=download) which consists of the marks secured by students in various subjects.

The dataset is stored in a csv file and will be imported into a pandas dataframe for the Part I of the project. Here, exploratory data analysis using Python data science and data visualization libraries will be used to explore the dataset’s variables, understand the data’s structure, oddities, patterns, and relationships, and answer some questions about the data. In the Part II of the project, a slide deck will be used for explanatory data visualizations that tells a story about the data exploration. The questions below have been answered through exploration. Also, the meaning of each variable in the dataset is stated;

**Questions**
- How effective is the test preparation course?
- Which major factors contribute to test outcomes?
- What would be the best way to improve student scores on each test?

**Variables**
- Gender - Gender of student 
- Race/Ethnicity - Race of student anonymized as groups
- Parental Level of Education - Parent Level of Education 
- Lunch - Free/reduced or standard lunch program
- Test Preparation course - Learning tool designed to increase student performance on standardized tests
- Math Score - Math score in test
- Reading Score - Reading score in test
- Writing Score - Writing score in test


## Data Wrangling

The dataset was downloaded manually from Kaggle and stored in a Pandas dataframe. Programmatic assessment was carried out to assess the data for errors. The following Quality and Tidyness issues were found and corrected as stated;

| Issues | Errors | Solution|
|--------|--------|---------|
|Quality | inadequate column headers | Rename columns |
|        | parental level of education datatype is object | Convert to CategoricalDtype |
|        | no unique identifier for observations | Create a new column *id* , fillin values by adding 1 to index, and convert to string |
|Tidyness | two variables from three columns: *math score*, *reading score*, *writing score* | Melt columns to *subject* and *score* |

## Summary of Findings

Following univariate explorations, the following were observed for each variable;

- *score* - A histogram revealing a non-uniform distribution of data points in different bins. Overall, a generally bimodal and slightly left-skewed distribution is observed.
- *test_prep* - A bar chart shows the mode status for test preparations are students that did not have any test preparation
- *subject* - A bar chart shows a uniform distribution of each subject. Students are tested in all subject represented in the dataset
- *gender* - The distribution is roughly unimodal, with the data representing more male than female students, although having little significant difference. 
- *lunch* - The most common lunch plan in the dataset is Standard. The difference in frequency is almost twice the antimodal lunch plan
- *parent_education* - There is a right skew in the data represented. The distribution is bimodal, with the most common Education level belonging to some college, high school, and associate's degree. 
- *ethnicity* - A bar chart shows the mode ethnicity for students in the dataset is group C. There is a consistent decrease in the representation of each ethnic group in this order (group C, group D, group B, group E, group A).

Next a comparison of independent variables with test scores and test preparations was carried out. Here's what is observed;

We found the median scores for female students were higher than male students. This can be attributed to the distribution of their scores in each subject where male student were observed to excel more in 1 out of the 3 subjects, Math. In opposition, female students excel at Reading and Writing.

For the  socio-economic effects; lunch plan, parent level of education and representation of ethnic groups, were used as metrics for household income level, and motivational support at home and school. It was observed that the higher the income and educational level at home, the higher the test scores.

On the part of support at school, the analysis revealed the most engagement with test preparations were found in the least represented ethnic group, group A. To further gauge the effect of test preparations, we investigated an interaction of each ethnic group to test preparations and its effect on test scores. 
We observed the median scores for completed test preparations are higher with each ethnic group compared to no test preparations. Also, in the box plot used to represent the data, the height of the IQR for group A is comparatively shorter in completed preparations than in no preparations. This suggests that students in group A for completed test preparation courses have a higher level of agreement in scores compared to the group A in no test preparations. 
We also compared the other two socio-economic factors; lunch plan and parent education with test preparation, to see the distribution in test scores, it was observed that although the test scores increased with a consistent rise of these factors, students who completed the preparatory course across these factors, obtained higher scores than students without a test preparatory course.



## Key Insights for Presentation

- In comparing the test preparations across the parent's education level, and ethnic group A, which is associated with a high rate of completing preparation courses, we have been able to measure how effective test preparation courses are by the notable difference in test scores seen across each group.

- We have also uncovered some determining factors of test outcomes. We know that subject plays a role by the distribution of scores in math to reading and writing based on the gender of the student. Socio-Economic factors like Lunch plan, which measures the household income of each student, Parent Level of Education which accounts for family environment and support, and Ethnicity which measures school support in minority represented groups are key factors in test scores. 

- Based on the data, to improve the test scores for students, I will suggest an increase in the engagement of test preparation courses, particularly on the subject each gender was shown to be weaker at, and an introduction of school related motivational and engagement activities targeted at students with low parental education background.