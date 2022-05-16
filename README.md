 # Group_5_Final_Project

## Selected Topic

* Selected Topic- We have opted to review and analyze crime statistics in service areas covered by the Charlotte Mecklenburg Police Department. We will use the data to assist the police department in resource planning and deployment. The primary resource impacted will be the officers themselves but the data will also help determine the optimal placement and use of technology and equipment. 

## Reason for Choosing the Topic

We chose this topic as each of the team members lives in the area and has a vested interest in public safety. This has become a more prevalent and pressing topic due to the area's steady growth. Although the growth is a sign of a healthy city and society it also comes with challenges and having effective law enforcement is a fundamental component in the city's continued success.  

## Project Objectives

Our goal is to develop a process to identify a response area's particular needs based on calls for service. We will look at the number of calls as well as the types of calls coming in from these response areas and align that information with officer experience and qualifications. We'll also look at the best allocation of vehicles based on the type needed as well as the supplies and gear that might be needed. 

## Data Sources

Our primary source of information will be the *City of Charlotte Open Data Portal* and we will also be pulling data from other sources deemed necessary to get the most complete picture.

## Questions and Considerations

The following list includes but is not limited to questions we will be asking and answering in order to make our determinations:

- Overall number of calls received by CMPD as well as number of calls within a particular Service Area
- Breakdown of calls by type or category overall as well as within a particular Service area
- Further breakout of calls by type or category as a percentage within a service area
- Calls by time of day both overall and within a particular service area
- Can certain types of calls be indicative of other types of crimes that might be occurring?
- Are there opportunities for other types of interventions and/or community outreach to reduce crime other than law enforcement? 
- Are there any comparable jurisdictions currently using a model that CMPD could emulate or leverage 
- It appears that calls currently have a high level classification of "Domestic Violence" and "Everything Else." Is there a way to further drill down on this data so that the "Everything Else" can be further distinguished
- What are some standard key metrics used by law enforcement agencies to resource plan as well as to determine what constitutes improvement in a particular area? 

To be clear we are not necessarily looking to predict future crimes rather we are trying to develop tools that provide real time crime data to identify areas of focus in order to reduce the crime rate. 

# Group 5 Final Project

## Machine Learning  
### Problem trying to solve   
Our goal is to create a supervised machine learning model to look at number of calls and types of calls coming in, in hopes that this information will allow better distribute of cops and supplies that may be needed based on the type of crime occuring. If successful, calls will be categorized as violent or non-violent calls which we can then map our geographically to find out where violent crime is most prominent.  
### Data needed  
The two primary datasets being used (Violent_Crime_Offenses.csv and CMPD_Calls_for_Service.csv) are both public and can be found and accessed through the Charlotte Open Data Portal (https://data.charlottenc.gov/). These datasets contain data from 2015 through 2022. Our expectation is to use the categorize violent crimes from incoming calls to help map out where violence in the Charlotte area is heaviest.
### Choosing and training the model  
We are using a supervised learning model that will continue to use our code with new, incoming data, and categorize it as we choose. We chose a supervised learning model because we know our data outcomes and plan on using both input and output data to benefit our goal. Our project scope falls under the classification subcategory for supervised learning because we will be applying labels to our data, categorizing areas based on our crime data. We will be using SKlearn and applying a logisitc regression to help classify our data. This will be used to decipher violent crimes from the calls for service. An example of what our sklearn machine learning code may look is picture below.

![sklearn_example](https://user-images.githubusercontent.com/96501958/168442833-9f2811c2-58ac-4276-95dc-be486bdf47d2.png)  


## Judging the Results

Ultimately the project will be considered successful when a reduction in crimes of various categories can be directly attributed to utilizing the technologies, languages, tools, and algorithms included in the project. In the short term success will be more attributed to proving that utilizing the technologies, languages, tools, and algorithms included in the project will lead to a reduction in crime.

## Reccomendations for Future Analysis

As a follow up for future analysis we might look at ways our project could be leveraged to provide other insights including expanding capabilities to identify trends and patterns that could help predict potential areas of concern. 

=======
![sklearn_example](https://user-images.githubusercontent.com/96501958/168442833-9f2811c2-58ac-4276-95dc-be486bdf47d2.png)

## Database

### Technology
As we work through this project, we will be utilizing PostgreSQL, a relational database, to store our tabular data. As we are looking to utilize 2-3 different CSV files, we will build tables for each to house our information and build relationships between them in pgAdmin. We will also be using SQLAlchemy to communicate between our databases and machine learning model. 

### Schema
The CSV files we will be using from Charlotte's Open Data Portal will require some editing down in Pandas to remove uneccesary or redundant columns and rows. 
As we explore and work with these datasets, we may find it beneficial to adjust these schemas to suit our needs. 

Our preliminary schema will look like this: 

![sample db schema](https://github.com/dannybarto/Group_5_Final_Project/blob/main/sample%20db%20schema.png)

![sample db layouts](https://github.com/dannybarto/Group_5_Final_Project/blob/main/sample%20db%20layouts.png)
 



We currently have 3 data sets from the City of Charlotte Open Data Portal that we will be looking at to complete our analysis. 

[Call Data](CMPD_Calls_for_Service.csv)


There are a few main data points that we will be examining:

- Calendar Year/Month - We plan to filter our data for a smaller subset of the time
- Geography ID/Location - The location of the call, incident or offense. ** More research will go into     making sure these we understand which ID's correspond to different neighborhoods/divisions in the city** 
- Call Count - number of calls coming in from specific locations in the city
- Call Description - type of call that is coming in, Domestic Violence or Patrol Call
- Offense Description - type of offense that has occured
- Offense Count - number of certain offenses occuring in that specific location 
- CMPD Patrol Division - designated patrol divisions that the CMPD has created in the city of Charlotte 
- Highest NIBRS Description - incident description based on the FBI NIBRS (National Incident-Based Reporting System) ** We will most likely condense/organize these incidents into categories**
- Clearance Status - the clearance status of the crime 











