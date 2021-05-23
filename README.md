# global-suicide-EDA
Data Exploration Project – R and Excel
## 1. Introduction
The number of people commits suicide has constantly appeared on many social media, web pages or television news, therefore, a simple question such as ‘are there a lot more people end their lives by suicide commitments?’ popped up in my head. According to the advance of data science, data visualization has become one of the key tools in making a big picture and analysing choices for human, consequently, the following question will be answered by data visualization approach.
• Which part of the world have the highest and lowest suicide from past to present?
• How does generation has an impact on suicide commitment?
• In what age range people are likely to commit suicide? • Does growth in GDP reflect the lower rate of suicide?
In order to answer the questions, R and excel are implemented to check the dataset, clean unformatted data into an appropriate form and deal with a missing value. For the sake of visualization, R and Tableau are utilised to illustrate and reflect the answer to the question.
## 2. Data Wrangling
The dataset needs some cleaning before visualization by using R and excel. This project uses the dataset from Kaggle with 27820 rows and 12 attributes (Master.csv, https://www.kaggle.com/russellyates88/suicide-rates-overview-1985-to-2016). The processing of this step is as follow:
Format Data Type: Use R to transform the type of attributes into applicable data type, for example, changing the data type of factor into integer or number.
Convert Meaningless Data Attribute: Use R to change the meaningless name of attribute since some of the data set are inconsistent.
Split and Delete Useless Data Attribute: Use R to remove unnecessary attribute to make the data set clean and simple to implement.
Deal with insufficient data: Use excels to see the trend and filter each category of the attribute in the data set if the amount of data is sufficient then applied R to eliminate insignificant data.
Tidy Data Frame: Use R to classify an untidy set of data into the proper class in the case that they are not such as class of age range, generation and gender.
## 3. Data Checking
For data checking, use R to show the overview of data and find missing value then excel to check outlier in each category to make it ready for data visualization.
Overview of attribute and data type: Use the function summary() in R to show data overview
![image](https://user-images.githubusercontent.com/70103737/119267587-ad7d7880-bc32-11eb-8390-e570affb7db9.png)
Missing value: As shown in Figure 1, there is no missing value or null since the data has been cleaned as described in the last section.
Outliers: Use excel to seeing whether there is an outlier on each category
After both processes, data wrangling and data cleaning, have been done, the data set is to be explored.
## 4. Data Exploration
In this step, the data set is visualized in different ways according to the question and to explore interesting patterns and trends on suitable visual by mainly using R. There are five parts consisted below on this section which the first thing is seeing the general trend of the data.
# 4.1 Global trend of Population, Suicide Rate and GDP per Capita
![image](https://user-images.githubusercontent.com/70103737/119267607-bd955800-bc32-11eb-88c4-f0454d7de025.png)
As you can see in Figure 2, the number of global populations rose sharply from the beginning then gradually increased around 1994 to 2002. After that reached its peak in 2010 and the number started falling from 2010 onward. Therefore, it can be concluded that the population keep decreasing.
![image](https://user-images.githubusercontent.com/70103737/119267623-c8e88380-bc32-11eb-92a6-683bbf19f943.png)
From Figure 3, suicide number increased significantly from 1985 onward and reached a peak when there was the highest suicide rate approximately in 1998. There is a convex curve after its peak and then the suicide rate gradually went down.
![image](https://user-images.githubusercontent.com/70103737/119267629-d1d95500-bc32-11eb-9524-992d9d8cb2f5.png)
As seen from Figure 4, GDP per capita steadily went up in the beginning and there is a sudden growth from 2002 to 2008. The GDP drop and increased again after 2010.
# 4.2 World part and the Suicide
This section will answer the first question which is ‘Which part of the world have the highest and lowest suicide rate form past to the present?’. To answer this question, we need to assign a continent for each country in the dataset since there is no determinant that could define the part. The world is separated into five continents and each continent has the colour as in the following:
![image](https://user-images.githubusercontent.com/70103737/119267644-e289cb00-bc32-11eb-9db4-4ffe26928f4e.png)
Dark Blue represents Africa
Orange represents the Americas
Red represents Asia
Light blue represents Europe
Figure 5 Green represents Oceania

![image](https://user-images.githubusercontent.com/70103737/119267655-ed446000-bc32-11eb-874c-517c5c9116ad.png)
According to the global map creating by Tableau in Figure 6, red circle represents the time suicide occur. The world map shows the part which has the highest number of red circles in Europe while the number of red circles in Asia and Oceania is quite similar. To see the clear picture, a bar graph of all the country in the dataset showing the suicide rate is introduced in the figure below.
![image](https://user-images.githubusercontent.com/70103737/119267669-f59c9b00-bc32-11eb-90db-ca68573e89b5.png)
The bar chart creating using Tableau categorized by continents show the suicide rate of 100k since the exact number is very low.
To be specific, from Figure 7, the country with the highest level of suicide commitment is Russian Federation which located in Europe. On the other hand, the lowest level of suicide commitment is in United Arab Emirate from Asia.
There is a large amount of the number of countries of Europe showing high rates of suicide while a few countries have less suicide rate. This can be considered as overrepresentation.

# 4.3 Generation and the Suicide
This section will answer the second question which is ‘How does generation have an impact on suicide commitment?’. In order to answer this question, we plot the bar graph using R to show the effect of generation on the number of suicide commitment
![image](https://user-images.githubusercontent.com/70103737/119267681-03eab700-bc33-11eb-9d2c-c245f1cd0b76.png)
From the bar graph above, we can see that Baby Boomers generation who were born just after world war II ("Baby Boomer", 2019) commit suicide the most comparing to the other generation. Surprisingly young people in generation z yield the lowest amount of suicide commitment. As being observed, the number of suicides keeps dropping from Baby Boomers generation onward which has the same trend related to global suicide in Figure 3.
![image](https://user-images.githubusercontent.com/70103737/119267691-0c42f200-bc33-11eb-98b0-506df6b7130e.png)
The graph illustrates how different generations reflect the different suicide number in every year. Most of the trend of the generation slightly increased, reached the highest point and fell, however, the trend of Generation X obviously fluctuates from time to time. For example, the uncommon trend of suicide number of Generation x in 2009 is one-third of the
number in 2010. This might be because of the world important event occurred at that time e.g. natural disaster, bombard or economic crisis leading to increasing in stress level and worse quality of people lives. Further research is needed to get a specific insight.
# 4.4 Age range and the Suicide
This section will answer the third question which is ‘In what age range people are likely to commit suicide?’. Using R to plot two graphs below will answer the question and using Tableau for another graph to forecast the trend of each age range.
![image](https://user-images.githubusercontent.com/70103737/119267717-27156680-bc33-11eb-9d69-14417a4439b4.png)
From the graph on the left-hand side, the suicide number has been plotted against the year for every age range showing in a different colour. Age 5-14 is likely to be the most stable group of suicide commitment while the number of Age 35-54 vary from the beginning which there is an observable rise in 19s to the peak around 2000 and then drop. Even though the number of suicides fell almost half comparing to the begin, it is clearly the highest number of suicides among the other group.
![image](https://user-images.githubusercontent.com/70103737/119267728-2e3c7480-bc33-11eb-9453-d4535e4d3274.png)

This second graph looks at the same question still show the other view of age range and suicide number by adding gender into the graph also this ensures that the result of the first graph is right. As you can see, there exists the normal distribution and the highest number of suicide commitment is in the age 35-54. Furthermore, most of the suicide is committed by Male in a very high amount.
![image](https://user-images.githubusercontent.com/70103737/119267737-35638280-bc33-11eb-8f49-6738b12814e6.png)
The graph above shows the trend of suicide commitment of different age range against the period of time and show the possible range that the number of suicides is likely to be in the future indicating in the blue. As you can see, the future trend of age 35-54 has a high probability of varying the most.
# 4.5 Gross Domestic Product and the Suicide
This section will answer the last question of the report which is ‘Does growth in GDP reflect the lower rate of suicide?’. GDP or gross domestic product is one important measure of economic activity in other words it represents how rich that country is. From the data obtained, there are two categories of GDP which are GDP per year and GDP per capita since GDP per capita includes nation’s overall population as a result GDP per capita represents a much better determination of living standard ("Difference Between GDP and GDP per Capita | Difference Between", 2019). Therefore, we solely interpret the dataset based on GDP per capita.
![image](https://user-images.githubusercontent.com/70103737/119267749-3dbbbd80-bc33-11eb-816e-d717a964b1fc.png)
Before plotting the graph, we cluster GDP per capita into high level or low level separated by a mean of overall GDP per capita in order to see the outcome clearly. The scatter plot in Figure 13 reveals that low GDP per capita yields the high level of suicide number on the blue part while where GDP per capita is higher reflects a lower number of suicide commitment.
## 5. Conclusion
This project has visualized the suicide trend in many different aspects in order to see trend and pattern that could answer the original question and might lead to some interesting discoveries about suicide commitment. The data wrangling and data checking are the first few steps to get data ready for exploration through transforming dataset into appropriate type and format then examine whether there are some errors or if the data show the similar pattern and finally checks the outlier. Using tools like R and Tableau improve the sense of exploration and yield meaningful visualization. The exploration part has answered all the question on the introduction list by presenting on a number of graphs on 4.2, 4.3, 4.4, 4.5. In addition, the general trend for global suicide commitment is illustrated in 4.1.
