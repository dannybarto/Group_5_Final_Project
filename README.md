# Group 5 Final Project

## Machine Learning  
### Problem trying to solve   
Our goal is to create a supervised machine learning model to look at number of calls and types of calls coming in, in hopes that this information will allow better distribute of cops and supplies that may be needed based on the type of crime occuring. If successful, calls will be categorized as violent or non-violent calls which we can then map our geographically to find out where violent crime is most prominent.  
### Data needed  
The two primary datasets being used (Violent_Crime_Offenses.csv and CMPD_Calls_for_Service.csv) are both public and can be found and accessed through the Charlotte Open Data Portal (https://data.charlottenc.gov/). These datasets contain data from 2015 through 2022. Our expectation is to use the categorize violent crimes from incoming calls to help map out where violence in the Charlotte area is heaviest.
### Choosing and training the model  
We are using a supervised learning model that will continue to use our code with new, incoming data, and categorize it as we choose. We chose a supervised learning model because we know our data outcomes and plan on using both input and output data to benefit our goal. Our project scope falls under the classification subcategory for supervised learning because we will be applying labels to our data, categorizing areas based on our crime data. We will be using SKlearn and applying a logisitc regression to help classify our data. This will be used to decipher violent crimes from the calls for service. An example of what our sklearn machine learning code may look is picture below.

![sklearn_example](https://user-images.githubusercontent.com/96501958/168442833-9f2811c2-58ac-4276-95dc-be486bdf47d2.png)
