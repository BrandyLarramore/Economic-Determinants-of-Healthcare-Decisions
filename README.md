# Economic Determinants of Healthcare Decisions
_Does a higher household income indicate a higher vaccination rate?_

## Table of Contents
- [Motivation](#Motivation)
- [Data Question](#Data-Question)
- [Research and Findings](#Research-and-Findings)
- [Challenges and Further Research](#Challenges-and-Further-Research)
- [Technologies and Data Sources](#Technologies-and-Data-Sources)

## Motivation
Prior to becoming a data analyst I worked helping people financially as a consultant. Financial education is something I’m really passionate about, as understanding how investing and mitigating debt can really alleviate suffering. My interest in the medical field, inspired by my mother's career as a nurse, has driven me to seek ways to contribute outside of the clinical environment. This project embodies my ambition to intersect medical and financial support, aiming to provide insights that can aid in both realms.

## Data Question
The primary question I sought to answer is this: Is there a correlation between income and vaccination status in America, and if so, what does it show?

This question seeks to understand if and how financial well-being influences healthcare decisions, particularly vaccinations received. Insights derived could inform policy decisions, healthcare education programs, and financial advising strategies, particularly in underserved communities. 

The intended audience includes healthcare professionals, policy makers, financial advisors, and public health researchers.

## Research and Findings
The first step was compiling data from the CDC and Census, I first explored the data using Excel.
Pivot tables were very helpful in identifying distributions of income and vaccinations. 
I used find and replace to fix errors in symbol transfer with the symbol ">" (greater than), changing the displayed symbols to instead say "or older" after the provided age.
Later, I sorted the data by State to manually add in state fips codes after needing to expand my research further.
After becoming better aquainted with the data, I created three python notebooks. The first objective was to join the data so that correlations could (hopefully) be drawn between the data sets. In order to have a comon key to join on, I used python to pull the last 5 fips numbers from the geography column of the income data. The vaccine data came with fips numbers provided.

After joining the two data sets and looking at different correlations, I found that there was not a clear correlation between income and vaccination rate alone. At this point I decided to expand my research further into looking for correlations in locations as well. 

I imported the data into Power BI to map the income and vaccination rates by state. Here is where I found a clear correlation when looking at the top and bottom income and vaccination rate states:

States with higher incomes frequently have lower vaccinations rates. The opposite is also true with states having lower incomes frequently having higher vaccination rates. Only one state, Arkansas, had both lower income and lower vaccination rates. There were no states in the higher incomes that had higher vaccination rates.


It's important to note that correlation does not two imply causation, and the observed relationship between income and vaccination rates is likely additionally influenced by a combination of other factors not explored in this project. Addressing disparities in vaccination rates requires a multifaceted approach that considers socioeconomic, cultural, and systemic factors to ensure equitable access to vaccines for all communities.


After the analysis was complete I spent a significant amount of my free time theorizing as to what could cause this unexpected correlation. A few of my theories include:

1) Access to additional healthcare options - Higher-income individuals may have access to alternative healthcare options, such as naturopathic or holistic medicine, which may lead them to prioritize alternative approaches to disease prevention over vaccination. Higher-income individuals may also perceive themselves to be at lower risk of vaccine-preventable diseases due to factors such as access to better healthcare, sanitation, and living conditions. As a result, they may underestimate the importance of vaccination for themselves and their communities.

2) Types of insurance - Lower income families may have state provided medical insurance instead of private insurance which could potentially have less copays, or barriers to access to vaccinations.



## Challenges and Further Research
When using data from two different sources it is common for the data to not have a lot of similarities. The Census data had 133 columns including columns that had already calculated relevant aggregations such as the average income. The CDC dataset only had 10 columns and looked at only 4 different types of vaccines. Because of this, it would be worthwile to look into finding data on additional vaccinations. Also, since we have all gotten the pleasure of experiencing our own pandemic, there was a shift in focus of vaccination data collection in 2020, focusing more on the COVID-19 vaccine, making data on a more broad range of vaccinations even more challenging to find.

I also think it could be helpful to explore the type of insurance used. I wonder if there are additional correlations when looking at state provided insurance and private insurance?


## Technologies and Data Sources
### Technologies
- Excel
- Python
- Jupyter Notebooks
- Power BI

### Data Sources
- United States Census Bureau 2019 Income: [Data Downloads](https://data.census.gov/table?q=income%20by%20county%20in%20the%20united%20states%202019)
- CDC Vaccination Coverage among Adults: [Data](https://data.cdc.gov/Vaccinations/Vaccination-Coverage-among-Adults-18-Years-/aetd-68ew/about_data)
