# Data-Visualization-on-CDC-dataset
Various types of data visualizations such as graphs, pie charts, line graphs, etc.
# Dataset Chosen:
The chosen dataset contains information about an adult's diet, physical activity and weight status from Behavioral Risk Factor Surveillance System. The data has 33 factors and 88,629 entries.
# https://chronicdata.cdc.gov/Nutrition-Physical-Activity-and-Obesity/Nutrition-Physical-Activity-and-Obesity-Behavioral/hn4x-zwk7

# Data Cleaning/ETL Process:
The first step was to delete any column with non-useful data. The second step was to find the missing data entries and work on them. The third step was to check errors in the entries such as leading and trailing spaces, duplicates, etc. with the help of a pivot table. The entire ETL process was done using MS Excel. The first observation was that the values for “YearStart” and “YearEnd” were the same, hence all entries were replaced by only one column named “Year”. The “Topic” column had entries similar to “Class”, so to avoid confusion only the “Class” column was kept. Additionally, “QuestionID” was similar to “Question”, “TopicID” to “ClassID”, “Data_Value_Alt” to “Data_Value”, “StratificationCategoryId1” to “StratificationCategory1” and “StratificationID1” to “Stratification1”. In each of the cases the prior columns were deleted. The “Datasource” entries are all same as the there is only one source for all the data. Similarly columns “Data_Value_Footnote_Symbol”, “Data_Value_Unit” and “Data_Value_Type” have all entries as the same value or data with no inference. Columns like “Data_Value_Footnote”, “Total”, “Age(years)”, “Education”, “Gender”, “Income” and “Race/Ethnicity” have a lot of missing values and can’t be used if the blanks are deleted hence these entire columns had to be deleted. The “StratificationCategory1” had a very few missing values and hence the blanks were deleted. In the same manner the blanks in columns “Data_Value” and “GeoLocation” were deleted. In all the cases the number of deleted entries was less than 10% of the entire dataset. The column “GeoLocation” was split into two columns “Latitude” and “Longitude” for ease of analysis. We did not use the data from “Data_Value”, “Low_Confidence_Limit”, “High_Confidence_Limit” and ”Location ID” columns hence they were deleted. After these changes the dataset had transformed to 11 factors and 78,199 entries. 

# Summary:
Through the multiple visualizations, we could see that Class, Question, and Stratification were the majorly used Columns. It helped link location and time (Years) to the other factors of the sheet to do the analysis. We found the factors about Nutrition and Obesity that impacted the study, made relationships, and drew conclusions for each of them individually. 
Multiple aspects such as age, income level, race etc. have had an impact on the study. The dataset had columns with multiple options to explore such as the categories in class, stratification and questions which helped to see the most and least impactful contributors. 
