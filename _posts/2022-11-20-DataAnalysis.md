---
layout: post
title: "Data Analysis - Data Processing with R"
subtitle: "Description of R Scripts for data processing."
background: '/img/posts/01.jpg'
---

### 01 Merging Excel files with equal structure with inherits.R

[R Script - Merge Excel Files with Inherits](https://github.com/albarey33/Data_Analysis_R/blob/main/01%20Merging%20Excel%20files%20with%20equal%20structure%20with%20inherit.R)

#### Brief Description:

Use Case: To import data on parts (due to source system limitations) and integrate them into one CSV file. The script first create a list of the required Excel files names located in the source folder by using list.files and regex to define a pattern. Then a function is defined to read the data inside the Excel files, this create tibbles. The function uses readxl::read_excel(filename). For convenience, the defined function also converts the logical fields to character using "inherits". Finally the tibbles are merged into one CSV using do.call bind_rows. 


___

### 02 Merging Excel files with equal structure with mutate across.R

[R Script - Merge Excel Files with Mutate Across](https://github.com/albarey33/Data_Analysis_R/blob/main/02%20Merging%20Excel%20files%20with%20equal%20structure%20with%20mutate%20across.R)

#### Brief Description:
. 
. 
. 

___

### 03 Merging CSV files equal structure.R

[R Script - Merge CSV files with equal structure](https://github.com/albarey33/Data_Analysis_R/blob/main/03%20Merging%20CSV%20files%20equal%20structure.R)

#### Brief Description:
. 
. 
. 

___

### 04 Merging CSV files different structure.R

[R Script - Merge CSV files with different structure](https://github.com/albarey33/Data_Analysis_R/blob/main/04%20Merging%20CSV%20files%20different%20structure.R)

#### Brief Description:
. 
. 
. 

___

### 05 Comparison and Changes between Two Periods.R

[R Script - Comparison and Changes between Two Periods](https://github.com/albarey33/Data_Analysis_R/blob/main/05%20Comparison%20and%20Changes%20between%20Two%20Periods.R)

#### Brief Description:
. 
. 
. 

___

### 06 Change Values based on External Table - Similar to Match Index.R

[R Script - Change Values based on External Table](https://github.com/albarey33/Data_Analysis_R/blob/main/06%20Change%20Values%20based%20on%20External%20Table%20-%20Match%20Index.R)

#### Brief Description:
. 
. 
. 

___

### 07 Join two Tables for Classification by Type of Practices.R

[R Script - Join two Tables](https://github.com/albarey33/Data_Analysis_R/blob/main/07%20Join%20two%20Tables%20for%20Classification%20by%20Type%20of%20Practices.R)

#### Brief Description:
. 
. 
. 

___

### 08 Apply changes to Cost fields.R

[R Script - Apply changes to Cost fields](https://github.com/albarey33/Data_Analysis_R/blob/main/08%20Apply%20changes%20to%20Cost%20fields.R)

#### Brief Description:
. 
. 
. 

___

### 09 Apply changes to Medical Condition fields.R

[R Script - Apply changes to Medical Condition fields](https://github.com/albarey33/Data_Analysis_R/blob/main/09%20Apply%20changes%20to%20Medical%20Condition%20fields.R)

#### Brief Description:
. 
. 
. 

___

### 10 Count of Member Months Matrix Melt DCast.R

[R Script - Count of Member Months Matrix Melt DCast](https://github.com/albarey33/Data_Analysis_R/blob/main/10%20Count%20of%20Member%20Months%20Matrix%20Melt%20DCast%20.R)

#### Brief Description:
. 
. 
. 

___

### 11 Split One Column into Two Fields.R

[R Script - Split One Column into Two Fields](https://github.com/albarey33/Data_Analysis_R/blob/main/11%20Split%20One%20Column%20into%20Two%20Fields.R)

#### Brief Description:
. 
. 
. 

___

### 12 Inputation using LeftJoin and Coalesce.R

[R Script - Inputation using LeftJoin and Coalesce](https://github.com/albarey33/Data_Analysis_R/blob/main/12%20Inputation%20using%20LeftJoin%20and%20Coalesce.R)

#### Brief Description:
. 
. 
. 

___

### 13 Match Replace Pattern ReGex.R

[R Script - Match Replace Pattern ReGex](https://github.com/albarey33/Data_Analysis_R/blob/main/13%20Match%20Replace%20Pattern%20ReGex.R)

#### Brief Description:
. 
. 
. 

___

### 14 Add Index column to data frame.R

[R Script - Add Index column to data frame](https://github.com/albarey33/Data_Analysis_R/blob/main/14%20Add%20Index%20column%20to%20data%20frame.R)

#### Brief Description:
. 
. 
. 

___

### 15 Examples BarPlots ggplot.R

[R Script - Examples BarPlots ggplot](https://github.com/albarey33/Data_Analysis_R/blob/main/15%20Examples%20BarPlots%20ggplot.R)

#### Brief Description:
. 
. 
. 

___

### 16 Date type recap by time periods Week Day Lubridate.R

[R Script - Date type recap by time periods](https://github.com/albarey33/Data_Analysis_R/blob/main/16%20Date%20type%20recap%20by%20time%20periods%20Week%20Day%20Lubridate%20.R)

#### Brief Description:
. 
. 
. 

___

### 17 Split string of values into multiple fields and summarize.R

[R Script - Split string of values](https://github.com/albarey33/Data_Analysis_R/blob/main/17%20Split%20string%20of%20values%20into%20multiple%20fields%20and%20summarize.R)

#### Brief Description:
. 
. 
. 

___

### 18 Merge multiple fields of labels into one.R

[R Script - Merge multiple fields of labels](https://github.com/albarey33/Data_Analysis_R/blob/main/18%20Merge%20multiple%20fields%20of%20labels%20into%20one.R)

#### Brief Description:
. 
. 
. 

___

### 19 Classification Categories using mutate.R

[R Script - Classification Categories using mutate](https://github.com/albarey33/Data_Analysis_R/blob/main/19%20Classification%20Categories%20using%20mutate.R)

#### Brief Description:
. 
. 
. 

___

### 20 Recap of Sparse Matrix Melt Dcast Conditions vs Periods.R

[R Script - Recap of Sparse Matrix](https://github.com/albarey33/Data_Analysis_R/blob/main/20%20Recap%20of%20Sparse%20Matrix%20Melt%20Dcast%20Conditions%20vs%20Periods.R)

#### Brief Description:
. 
. 
. 

___

### 21 4C Read data Interactions_WEEK_26_2021.R

[R Script - Merge Excel Files](https://github.com/albarey33/Data_Analysis_R/blob/main/21%204C%20Interactions_WEEK_26_2021.R)

#### Brief Description:
. 
. 
. 

___

### 22 4C Merge data Interactions_All_Periods.R

[R Script - Merge Excel Files](https://github.com/albarey33/Data_Analysis_R/blob/main/22%204C%20Interactions_All_Periods.R)

#### Brief Description:
. 
. 
. 

___


