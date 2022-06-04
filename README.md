# Group_5_Final_Project

## Introduction

As residents of Charlotte, NC, our team took a personal interest in looking at and analyzing crime statistics reported by the Charlotte Mecklenburg Police Department. Charlotte is a fast-growing city. Over the last few years there has been a major influx of residents, coming to North Carolina for the reasonable cost of living and vast job opportunities. The data spans over the last 7 years, but the last few years have been particulary unqiue with a global pandemic and political unrest. With all these factors in mind, we were interested in discovering any trends that have developed over the last few years. With the safety of our city in mind, our main goal was to give insight to the CMPD on where and when crime is happening most frequently and how violent are the majority of those incidents. The data looks at the different patrol divisons in which incidents are occurring and also is categorized by what type of crime is involved. These points alone would be able to tell us where the Police department should allocate more resources and potentially which types of resources are needed.
 

## Project Objectives

Our project objective is to better inform the Charlotte Police Department on where to allocate their resources best. By looking at where and when the most dangerous incidents are happening, the CMPD would be able to know which patrol divisions need the best reinforcement. Whether they station officiers in cars vs. bikes, or send officiers to the scene with more backup or not; these are the types of questions we would like to add more insight to. We were interested in also looking at the time frame in which more crimes occur. Knowing what time of year more crime, or more violent crime, is occuring would also help the CMPD with resource planning.

## Questions and Considerations

The following list includes but is not limited to questions we will be asking and answering in order to make our determinations:

- In which Divison/Patrol ID are crimes occuring the most? Is there a patrol Divison that holds the most violent crime and does that differ from the overall number?
- What is the most frequent type of crime occuring in the Charlotte area?
- Is there a season in which crime is the highest?
- How has the number of incidents been changing over the last few years?
- Is there a type of location, in which crime is the highest. (ex. residential vs. commercial, etc)
- How much violent vs. non-violent crime is there?

To be clear we are not necessarily looking to predict future crimes rather we are trying to give insight and indentify areas of focus to help the CMPD reduce crime rate.

## Data Sources

Our primary source of information is the [City of Charlotte Open Data Portal](https://data.charlottenc.gov/)

We looked at the CMPD Incident report data primarily. This data set was so vast, that we decided to break this into 3 different tables for our analysis.
To view these tables, you can access them by the below link as they were too large to upload to GitHub.

[OneDrive](https://onedrive.live.com/?authkey=%21ACsCHxuzouAm0bk&id=271B512C5492C5E1%21240915&cid=271B512C5492C5E1)

[Incident Data](CMPD_Incidents.csv)

There are a few main data points that we will be examining:

- Incident Report ID - This is the unqiue identifier for each incident reported. 
- Year/Month- We used this to filter our data for different time periods/seasons 
- Divison ID - These are the unique patrol divisons that the CMPD separates the city by
*insert divison picture here*
- Type of Location - This distinguishes the locations between residental, public, commerical, retail and open area
- Highest NIBRS Description - incident description based on the FBI NIBRS (National Incident-Based Reporting System)
  *For a full list of the Incident codes and what crimes they are related to, visit:  [FBI NIBRS User Manual](https://www.fbi.gov/file-repository/ucr/ucr-2019-1-nibrs-user-manua-093020.pdf/view)
- Violent/Non-Violent - distinguishing between violent and non-violent crime
- Clearance Status - the clearance status of the crime 

## Methodology and Results 

### Data Cleaning 

To clean the data we used Python and Pandas, to set up 3 clean tables to work with. Since this data is reported and inputed from officers or staff, we had to account for a lot of human error. We had to clean up the spelling of city names and division ids, eliminate null values and also categorize the different NIBRS codes into violent vs. non-violent. 

### Database 

#### Technology
As we work through this project, we will be utilizing PostgreSQL, a relational database, to store our tabular data. As we are looking to utilize 2-3 different CSV files, we will build tables for each to house our information and build relationships between them in pgAdmin. We will also be using SQLAlchemy to communicate between our databases and machine learning model. 

#### Schema
The CSV files we will be using from Charlotte's Open Data Portal will require some editing down in Pandas to remove uneccesary or redundant columns and rows. 

As we explore and work with these datasets, we may find it beneficial to adjust these schemas to suit our needs. 

Our preliminary schema will look like this: 

![sample db schema](https://github.com/dannybarto/Group_5_Final_Project/blob/main/sample%20db%20schema.png)

![sample db layouts](https://github.com/dannybarto/Group_5_Final_Project/blob/main/sample%20db%20layouts.png)

### Machine Learning  ###

#### Problem trying to solve   
Our goal is to create a supervised machine learning model to look at number of calls and types of calls coming in, in hopes that this information will allow better distribute of cops and supplies that may be needed based on the type of crime occuring. If successful, calls will be categorized as violent or non-violent calls which we can then map our geographically to find out where violent crime is most prominent.  

### Choosing and training the model  
We are using a supervised learning model that will continue to use our code with new, incoming data, and categorize it as we choose. We chose a supervised learning model because we know our data outcomes and plan on using both input and output data to benefit our goal. Our project scope falls under the classification subcategory for supervised learning because we will be applying labels to our data, categorizing areas based on our crime data. We will be using SKlearn and applying a logisitc regression to help classify our data. This will be used to decipher violent crimes from the calls for service. An example of what our sklearn machine learning code may look is picture below.

![sklearn_example](https://user-images.githubusercontent.com/96501958/168442833-9f2811c2-58ac-4276-95dc-be486bdf47d2.png)  


## Dashboard - Tableau

[Tableau Story Board](https://public.tableau.com/app/profile/brittany.marchand/viz/Group-5-CMPD-CrimeData/CMPDCrimeData?publish=yes)


## Recommendations for Future Analysis

There are a few ways this analysis could be improved upon and continued. 
Future analysis could include the following additions: 
- Adding population data into this analysis in order to compare if growing crime trends are only related to population growth or other factors.
- For the machine learning model: 











