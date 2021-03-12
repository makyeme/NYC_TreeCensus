# NYC_TreeCensus



## Table of contents
- [GeneralInformation](#generalinformation)
- [Technologies](#technologies)
- [Setup](#setup)
- [Conclusion](#conclusion)



## 1. General Information
The aim of this project is to generate  a cleaned out and comprehensive dataset from the NYC tree Census dataset.  The generated dataset will provide deeper  insights into quantitative and qualitative distribution of tree species and their health. It will be used address ecology and climate challenges within New York city.

Some of the questions I tried to explore through the data are outlined below:

- What is the target/dependant variable(s) to select and assess?
- What to do with missing values?
- What predictor/independent variables to keep for future model development?
- what depth of data cleaning should be applied?



## 2. Technology

This project was created with:

- Anaconda virtual environment version: 4.9.2
- anaconda-navigator version: 1.10.0
- Python version: 3.8.5
- Jupyter notebook version: 6.2.0
- Numpy library version: 1.19.2
- Matplotlib library version: 3.3.4
- Pandas library version: 1.2.1
- Seaborn library version 0.11.0 



## 3. Setup

The entire data cleaning processes and generation of a CSV file was excuted through 5 functions as detailed below:
NYC_TreeCensus.ipynb file contains all the codes for the above stated fucntions, 
It is available at [Github/makyeme](https://github.com/makyeme/NYC_TreeCensus/blob/main/missing_data.PNG)

### i. getData() Function

This function when called is able to 
- pull the dataFrame 
- strip whitespace from cells that have a string-like object in them

Libraries used: pandas

 
 ### ii. exploreData() Function 
 
when called, returns exploratory information on the dataFrame, information such as:
- number of observations
- variable names of dataFrame
- sum of missing values per variable
- data types of variables

Libraries used: pandas
 
 ### iii. getMissing() Function
 
when called, returns a dataframe with missing data percentage per variable and plots it
The NYC tree census dataset obtained contains some missing values. Missing values per variable/column are shown below.


![Optional Text](https://github.com/makyeme/NYC_TreeCensus/blob/main/missing_data.PNG)


Libraries used: Matplotlib, Seaborn, Pandas

### iv. cleanData() Function

when called, returns a fairly cleaned out dataFrame for further data analysis.
Whilst cleaning out the data, a set of decisions was taken, the rationale behind these decisions is elaborated below:

- I replaced all nan values  of the data set  with the category Dead. Data obtained from the documentation of the NYC tree census indicates that empty cells represent tress that were observed as dead or stumps. It is therefore justified to categorise missing values as ‘Dead’. We are therefore able to retain data on dead trees rather than excluding it. This data can be insightful.

- I decided to retain  all variables after imputing the missing values, in this way, we have a more insightful dataset

- No duplicates were found in the dataset

Libraries used: Pandas


### v. createCsv() Function 

when called Saves cleaned out dataframe to csv formart

libraries used: pandas



## 4. Conclusion

The project was an in-depth exercise to explore and clean data in the NYC Tree census dataset. Through the course of the project, I deepened my expertise in several data: exploration, cleaning, engineering and visualization techniques.

 
### Future directions:

- The dataset contains a wide variety of variables, there is more potential to consolidate select variables, especially those that carry simillar information. In this way, we can avoid duplication of information generated by variables.
- There is room for generating additional data visuals, to gain deeper insights in underlying trends of the dataset.
