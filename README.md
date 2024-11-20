# Beyond_Income_Engelberger
**Dataset Name**: Beyond Income
**Author Info**: Tia Enelberger - University of Calgary Student - tia.engelberger@ucalgary.ca
**Data Collection**: Collected September 2024- November 2024, data originally from 2021
**Geographic Location**: Calgary, Alberta Canada

**Key Topics**: Rent, Affordability, Vacancy Rates, New Construction, Secondary suites, Income

All the data used is compiled in the All_Data_CT_Matched excel

**Methods**
There is a total of six metrics used in this indicator to measure the reality of the housing market in Calgary. Each dataset used was for the 2021 year as this is the most recent census for Canada. The datasets used are as follows: New housing starts, average rent prices, household income, number of secondary suites, vacancy rates, and housing affordability. All of which are cited in the reference section. URL redirection does not allow for a specific URL to each specific dataset so below are the steps needed to get to the data.
Housing Affordability: Click URL → Core Housing Need Drop Down → Housing Standards
Average Rent: Click URL → Primary Rental Market → Average Rent ($)
Vacancy Rate: Click URL → Primary Rental Market → Vacancy Rate (%)
Household Income: Click URL → Population, Households and Housing Stock → Household Income

For the household income, a percentage was made by dividing the number of households with the income bracket $40,000 – $59,000 over total households for that census tract and multiplying it by 100. This bracket was used as the median income for an individual in Calgary before-tax is $44,440 [1]. The secondary suite dataset was a point dataset so the Summarize Within Geoprocessing tool was used to count the points within each census tract. 

To rank the data each factor used natural breaks (Jenks) to better estimate groupings. Each variable had 5 classes which were ranked 1-5. Household income was not ranked as you cannot rank based on the census data provided. After each of the five variables were ranked, they were averaged. The closer they are to 1 the more sustainable for an individual it is. No coding was used to rank each factor so the factor that was the least complete was used to rank all variables. In this case vacancy rate only had a handful of numbers so it was used. There are a few counter-intuitive ranks that need to be explained. First, the secondary suite ranking descended from 5 corresponding to the lowest number (a rank of 5 for the class 0-5). It is predicted that lower rent and increased supply can be attributed to an increase in secondary suites, so a low number of secondary suites does not bode well for an individual. Vacancy rates were ranked in a similar way, a healthy vacancy rate is between 5-10% with low vacancy being worse than high for renters [2].  

**References** --> All references are in the included written report in the dataset
(1) The City of Calgary, “Data about Calgary’s population,” https://www.calgary.ca, 2021. https://www.calgary.ca/research/population-profile.html 
[2] JPMorgan Chase Bank, “Vacancy Rate: What Is It and How Does It Work? | Chase,” www.chase.com. https://www.chase.com/personal/mortgage/education/finding-a-home/vacancy-rate 
[3] Canada Mortgage and Housing Corporation. 2022.  New Housing Construction, CSV. Retrieved from https://www03.cmhc-schl.gc.ca/hmip-pimh/en/TableMapChart/Table?TableId=2.1.31.3&GeographyId=0140&GeographyTypeId=3&DisplayAs=Table&GeograghyName=Calgary#All 
[4] Canada Mortgage and Housing Corporation. 2022.  Household Income, CSV. Retrieved from https://www03.cmhc-schl.gc.ca/hmip-pimh/en/TableMapChart/Table?TableId=2.1.31.3&GeographyId=0140&GeographyTypeId=3&DisplayAs=Table&GeograghyName=Calgary#All 
[5] Alberta Government. 2021. Alberta Census Boundaries – Current, Shapefile. Retrieved from https://open.alberta.ca/opendata/gda-4d939041-851b-4848-bd30-44dbf129e16c 
[6] Canada Mortgage and Housing Corporation. 2022.  Average Rent, CSV. Retrieved from https://www03.cmhc-schl.gc.ca/hmip-pimh/en/TableMapChart/Table?TableId=2.1.31.3&GeographyId=0140&GeographyTypeId=3&DisplayAs=Table&GeograghyName=Calgary#All 
[7] Canada Mortgage and Housing Corporation. 2022.  Vacancy Rate, CSV. Retrieved from https://www03.cmhc-schl.gc.ca/hmip-pimh/en/TableMapChart/Table?TableId=2.1.31.3&GeographyId=0140&GeographyTypeId=3&DisplayAs=Table&GeograghyName=Calgary#All 
[8] Canada Mortgage and Housing Corporation. 2022.  Housing Standards, CSV. Retrieved from https://www03.cmhc-schl.gc.ca/hmip-pimh/en/TableMapChart/Table?TableId=2.1.31.3&GeographyId=0140&GeographyTypeId=3&DisplayAs=Table&GeograghyName=Calgary#All
