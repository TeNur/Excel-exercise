# Excel-exercise
Data analysis in Excel, analysing small LAX airport operational dataset

The purpose of this analysis was to analyse the data from the airport's point of view, focusing on overall operational aspect of the airport.
 **The goal was not to visualise and analyse all the available datapoints**; instead, I wanted to answer the key questions arising from the dataset in just a few charts. I also wanted to add a note of my findings and what actions I would recommend the airport to take following my analysis. 

Key questions that I defined from the data available:

- Totals: Volume of flights that have operated / Number of destinations / How many cancellations and delays there have been 
- Cause: What is the cause of cancellations and delays
- Top and bottom operators: Which airlines are at the top / at the botton of each performance metric

There was data available in the dataset such as flight lenght and departure delay which I chose not to use, as it gives no valuable information of the airport operations nor the airline functions. Flight lenght and flight speed depend on the destination, the type of aircraft used and other factors that are not necessary valuable to be calculated on average level.
Departure delay may happen due to myriad of factors (ground operations, delayed inbound flight, unruly passenger, slow boarding) and often airlines are able to catch up on delays once airborne. As such the focus in the analysis was on arrival delays.

Steps taken in analysis:

1. Viewed the dataset, read through the headers to understand the type of data available. Checked if there are null values, which there were not.
2. Did some basic calculations and added columns in the dataset to extract more information:

- Weekday, WeekNumber, MonthNumber = extracted this data from the date to allow quick filtering of date. I know this step is not necessary with PivotTables as they allow filtering through date automatically, but this was for my own purpose of handling the data

- Scheduled departure hour = extracted the hour from Departure Hour column, making it easier to analyse count of flights per hour

- Lenght hr, Meal, Average Speed = calculated this data utilising existing data. For Meal, I added a IF-statements that analyse the flight lenght and assess if a meal is offered onboard.

- Status, Delay type, Compensation = I added IF-statement utilising data from other columns. For Status, I assessed that if arrival delay is more than 15 minutes, the delay flight is delayed - delays less than this can be considered normal operational fluctuation. If delay is less than 60 minutes, it can be considered a moderate delay. A delay over an hour can be considered Major and over 2 hours Severe. For Compensation, I assessed if a flight is Cancelled due to National Air System OR the flight is Severely delayed, compensation is due.

3. I then created a separate sheet for 2016 analysis to forecast operations. My initial idea was to include this calculation in the final report but decided against as it is speculative data contrary to factual data analysis that I wanted to represent in the final report.

4. I then started create pivot tables to analyse the numbers, understand what charts would look like and put together my final report. Picture of the report can be found in this repository (LAX operations.jpg)

