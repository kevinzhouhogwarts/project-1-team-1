# Exploratory Data Analysis on Life Expectancy

Group 1 - Caitlin Hartley, Kevin Zhou, Rajamani Muthuraman, Rituparna Nandi
***

## Proposal & Background
While life expectancy is generally recognized to be positively correlated with GDP and other traditional measurements of economic development, there exist noticeable differences in life expectancy even among developed economies such as the high-income member countries of the OECD. What other factors, in addition to GDP, may significantly impact life expectancy, thereby giving rise to the differences in life expectancy seen among the cohort of deveoped countries?

***

## Project Overview
In order to obtain detailed data regarding life expectancy, GDP, and other potentially relevant health, social, and economic factors that spanned a long enough time period to be able to observe significant changes, we looked to several different sources. After using pandas to clean each obtained dataset, then merging them with the core life expectancy dataset, we visualized data using the matplotlib and plotly libraries.

***

## Data Sources and Cleaning

We used a curated dataset found on Kaggle, which contained data sourced from WHO, to explore variables that may impact life expectancy. While the data selection and range was mediocre, it gave us an idea to explore the variation in life expectancy among countries. An exploratory analysis of countries that had experienced the greatest and the least increase in life expectancy during the data's time period allowed us to narrow our focus to variation in life expectancy between countries at similar development profiles.
We also explored the difference in life expectancy between men and women as well as over the time period in which data was readily available from the UN World Population Prospects 2024 data report. However, the analysis was deemed to be only tangentially related to our main question.
Raw data is saved in /Resources/ directory. It includes:
- Life expectancy data since 1950 from the UN
- Causes of death data from the Global Burden of Disease study carried out by the Institute for Health Metrics and Evaluation (IHME) at the University of Washington
- Health expenditure data from the WHO
- GDP data from the Maddison Project Database 2020 at the University of Groningen
- Health expenditure data gathered via API request from the OECD
- Assorted socioeconomic global development indicators from the World Bank

Processes for cleaning raw data are saved in /cleaning_code/ directory. Cleaned data has been outputted to csv and saved in the /output/csv/ directory.
Since multiple data sources were used, the merge_master notebook in the parent directory was used to merge the cleaned indicator data (health, GDP, etc.) to the life expectancy data based on country and year.
***
## Analysis
Processes for analyzing the output, cleaned data to obtain conclusions are saved in /analysis/ directory and and charts are saved in /output/graphs/ directory.
Our analysis focused on Life Expectancy for OECD countries, based on GDP, Health Expenditure, and Health Factors such as Substance abuse, Diseases, Injuries and Health Care coverages. We dealt with main 
question - Why do OECD countries have variation in life expectancy? Specifically, why does the US have lower life expectancy compared to other wealthy countries in more recent years?

- We picked up top 15 wealthiest countries and saw how Life Expectancy is getting changed over time. We 
observe there is Steady rise in life expectancy across the top 15 wealthiest countries. But United States has experienced a stagnation in life expectancy over the past 20 years

![Life Expectancy Over Time for Top 15 Wealthiest Countries](output/graphs/image.png)

- We also have done statistical analysis for the same 15 countries, below is the result attached:
  
![Statistical Analysis of Life Expectancy for the 15 wealthiest countries](output/graphs/image-1.png)

- We also treid to see how Life Expectancy co-relates to GDP. The correlation between GDP per Capita and Life Expectancy has come out to be 0.7, indicating a strong, positive correlation exists between these two variables
  
![Life Expectancy vs. GDP per Capita in 2021](output/graphs/image-2.png)

- Next we delved into Health Expenditure to see if that can impact Life Expectancy. This analysis proved rgar over recent years, United States has increasing Health Expenditure per Capita but stagnating Life Expectancy compared to other wealthy OECD countries
  
![Life Expenctancy vs. Health Expenditure for the 15 Wealthiest countries](output/graphs/image-3.png)

- Also Correlation graph between Life Expectancy and Healh Expenditure has shown thatr United States is an outlier with very high Health Expenditure per Capita but low Life Expectancy compared to other wealthy OECD countries
  
![Correlation between Life Expenctancy vs. Health Expenditure](output/graphs/image-4.png)

***
## Conclusions

