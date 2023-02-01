---
layout: post
title: "Data Analysis - Data Processing with R"
subtitle: "Description of R Scripts for data processing."
background: '/img/posts/ds_scripts/back01.jpg'
---

### 01 Merging Excel files with equal structure with inherits.R

[R Script - Merge Excel Files with Inherits](https://github.com/albarey33/Data_Analysis_R/blob/main/01%20Merging%20Excel%20files%20with%20equal%20structure%20with%20inherit.R)

<!--- #### Brief Description: --->

The purpose of this script is to import data on parts (whenever there are limitations to get data) and integrate them into one CSV file. The script first create a list of the required Excel files names located in the source folder by using list.files and regex to define a pattern. Then a function that includes readxl::read_excel(filename) is defined to read the data inside the Excel files, creating tibbles (data tables). For convenience, the defined function also converts the logical fields to character using "inherits". Finally the tibbles are merged into one CSV using do.call bind_rows.


___

### 02 Merging Excel files with equal structure with mutate across.R

[R Script - Merge Excel Files with Mutate Across](https://github.com/albarey33/Data_Analysis_R/blob/main/02%20Merging%20Excel%20files%20with%20equal%20structure%20with%20mutate%20across.R)

Similar to the previous script but using where - accross instead of inherit to read and merge excel data files.


___

### 03 Merging CSV files equal structure.R

[R Script - Merge CSV files with equal structure](https://github.com/albarey33/Data_Analysis_R/blob/main/03%20Merging%20CSV%20files%20equal%20structure.R)

This script differs from the previous ones on the format of the source files. In this case the data source is in CSV format.

___

### 04 Merging CSV files different structure.R

[R Script - Merge CSV files with different structure](https://github.com/albarey33/Data_Analysis_R/blob/main/04%20Merging%20CSV%20files%20different%20structure.R)

This script is applied whenever there are two data sources in csv with different structure of fields. It contains a function that shows the fields that differs in names or is present in only one of the data sources. Using dplyr::rename is possible to match back the names so the fields can merge.

___

### 05 Comparison and Changes between Two Periods.R

[R Script - Comparison and Changes between Two Periods](https://github.com/albarey33/Data_Analysis_R/blob/main/05%20Comparison%20and%20Changes%20between%20Two%20Periods.R)

In this example the script identifies patients present in one of the two periods and absent in the other, either because the patient was new or was unenrolled. With table and group_by is possible to tally the numbers and associate these with, for example, the practices they were linked to.

___

### 06 Change Values based on External Table - Similar to Match Index.R

[R Script - Change Values based on External Table](https://github.com/albarey33/Data_Analysis_R/blob/main/06%20Change%20Values%20based%20on%20External%20Table%20-%20Match%20Index.R)

Similar to Match Index in Excel, with this script data is taken from another table to apply to specific records using a common key on these two tables. In this example we update the names of practices which come with outdated names from the source. The new names are kept in a specific table. This is also known as imputation of values. In this script a specific function was coded with the function "match" (base).

___

### 07 Join two Tables for Classification by Type of Practices.R

[R Script - Join two Tables](https://github.com/albarey33/Data_Analysis_R/blob/main/07%20Join%20two%20Tables%20for%20Classification%20by%20Type%20of%20Practices.R)

This script shows also a method to imputate values, but in this case the table that contains the data to update, let's say new names, doesn't come from a table hardcoded in the same script, but it is imported. In this example we assign a classification of practices by type: Family, Pediatric, etc. The way to imputate the values in this script is using left_join.

___

### 08 Apply changes to Cost fields.R

[R Script - Apply changes to Cost fields](https://github.com/albarey33/Data_Analysis_R/blob/main/08%20Apply%20changes%20to%20Cost%20fields.R)

This script applies a regular expression defined in a function to convert currency values in a text with a dollar sign "$0,000" into numeric format.

___

### 09 Apply changes to Medical Condition fields.R

[R Script - Apply changes to Medical Condition fields](https://github.com/albarey33/Data_Analysis_R/blob/main/09%20Apply%20changes%20to%20Medical%20Condition%20fields.R)

For only the fields related to medical conditions in the data, the empty or N/A values are replaced by the value "No". This changes are applied using dplyr functions rename, mutate and case_when.

___

### 10 Count of Member Months Matrix Melt DCast.R

[R Script - Count of Member Months Matrix Melt DCast](https://github.com/albarey33/Data_Analysis_R/blob/main/10%20Count%20of%20Member%20Months%20Matrix%20Melt%20DCast%20.R)

This code calculates the number of months each patient was enrolled in the last 12 months. For ilustration the script shows a calculation for only the enrollment month and the previous one. So a patient can have one or two member-months. The data comes in just two fields: Period and MID (patient identifier). Then the functions melt and dcast (equivalent of pivot tables) are used to convert the data into a table MID vs Period. Then fields of member-months are created per ending period.

___

### 11 Split One Column into Two Fields.R

[R Script - Split One Column into Two Fields](https://github.com/albarey33/Data_Analysis_R/blob/main/11%20Split%20One%20Column%20into%20Two%20Fields.R)

Split one field into two by using the function str_split_fixed (stringr) and a separator. In this example per each practice it was required to separate the National Provider Identifier (NPI) from the name.

___

### 12 Inputation using LeftJoin and Coalesce.R

[R Script - Inputation using LeftJoin and Coalesce](https://github.com/albarey33/Data_Analysis_R/blob/main/12%20Inputation%20using%20LeftJoin%20and%20Coalesce.R)

Another example of imputation of missing values but in this case using the information located in the same data table, for the same MID but in other periods. This is used on demographic values as for example race, DOB, that we can assume don't change for the same individual. A table without missing values is created using dplyr::group_by. Then the original data is merged with dplyr::left_join(). Finally the replacing value is taken with coalesce.

___

### 13 Match Replace Pattern ReGex.R

[R Script - Match Replace Pattern ReGex](https://github.com/albarey33/Data_Analysis_R/blob/main/13%20Match%20Replace%20Pattern%20ReGex.R)
Application of regular expressions to change the format of zip codes with 5-4 digits to 5 digits. Change of date format. Filter values with a string in the pattern by using grep (base). 

___

### 14 Add Index column to data frame.R

[R Script - Add Index column to data frame](https://github.com/albarey33/Data_Analysis_R/blob/main/14%20Add%20Index%20column%20to%20data%20frame.R)
An index column with unique values was created to use insted of the patients identifier MID or the name. It can be created either by using stringr::str_pad() or stringf (base).

___

### 15 Examples BarPlots ggplot.R

[R Script - Examples BarPlots ggplot](https://github.com/albarey33/Data_Analysis_R/blob/main/15%20Examples%20BarPlots%20ggplot.R)
This charts show the changes in the population enrollment, the ED, IP Visits and Readmissions in the previous 12 months. There were used either barplots or ggplot, geom_bar to compare both.  

___

### 16 Date type recap by time periods Week Day Lubridate.R

[R Script - Date type recap by time periods](https://github.com/albarey33/Data_Analysis_R/blob/main/16%20Date%20type%20recap%20by%20time%20periods%20Week%20Day%20Lubridate%20.R)
This script shows some applications of the lubridate package, to change the date formats, or to extract the year and months of the date values to summarize interactions. Also to add the weekdays or number of week on the year. 

___

### 17 Split string of values into multiple fields and summarize.R

[R Script - Split string of values](https://github.com/albarey33/Data_Analysis_R/blob/main/17%20Split%20string%20of%20values%20into%20multiple%20fields%20and%20summarize.R)
In the example there is a field with the reasons for service each interaction had. The most cases have grouped by commas two or more reasons. In order to split this values so that we can tally the total number of reasons for all the patients in a period, by using: with(dfRecapNoUTR, strsplit(Reason.s..for.Service, ',')). It splits the field into a list of lists. These lists are then converted into a sparse matrix to summarize it.

___

### 18 Merge multiple fields of labels into one.R

[R Script - Merge multiple fields of labels](https://github.com/albarey33/Data_Analysis_R/blob/main/18%20Merge%20multiple%20fields%20of%20labels%20into%20one.R)
The purpose of this script is the inverse of the previous one. With multiple medical conditions in the data, with one field per condition, the script takes per each MID the conditions on which each patient is flagged as "Yes". The script take the names of those flags and merge all those fields using apply-collapse. Finally all the resulting consecutive commas are removed with a regular expression.

___

### 19 Classification Categories using mutate.R

[R Script - Classification Categories using mutate](https://github.com/albarey33/Data_Analysis_R/blob/main/19%20Classification%20Categories%20using%20mutate.R)
Use mutate to add helper columns, then group_by to get a recap of interaction classification by categories. This method is similar to the Excel pivot tables. 

___

### 20 Recap of Sparse Matrix Melt Dcast Conditions vs Periods.R

[R Script - Recap of Sparse Matrix](https://github.com/albarey33/Data_Analysis_R/blob/main/20%20Recap%20of%20Sparse%20Matrix%20Melt%20Dcast%20Conditions%20vs%20Periods.R)

To export and visualize Power BI. Count of the number of visits performed more than a year before (> 365 days), by reading the date of the last visit per patient. It contains a function with Melt Each for Group of Conditions. With melt. It uses melt and group_by to get the final recap. Finally, the script shows a ggplot geom_line as an example of patients with hypertension by month.

___

### 21 Read data Interactions_WEEK_26_2021.R

[R Script - Merge Excel Files](https://github.com/albarey33/Data_Analysis_R/blob/main/21%204C%20Interactions_WEEK_26_2021.R)
Automatically read all the files containing the interactions per care manager in the last week. A tibble is created per file. All the tibbles are merged with dplyr::bind_rows to create a unique data frame for the week.  

___

### 22 Merge data Interactions_All_Periods.R

[R Script - Merge Excel Files](https://github.com/albarey33/Data_Analysis_R/blob/main/22%204C%20Interactions_All_Periods.R)
It collects all the weeks saved with the previous script. It collects and applies all the previous scripts. The resulting CSV files serve as sources for other procedures and for PowerBI dashboards.

___


