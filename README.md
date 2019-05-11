# ETLproject - TECHNICAL REPORT- Crime Data Analysis

## Introduction

We analysed the crime data for two large US cities, namely Boston, Los Angeles. For the scope of this project, we concentrated on July and September 2015 data. We took two datasets from two different sources mentioned below and transformed them to create the dataframes about the Incident Details, Offense Details and the Location Details. We loaded the analysed data into the sqlite database.  
Loaded table data is used to Visualize such as "To find out the top types of offenses" , "Heat map of where the crimes happened in respective cities". 

## Extract 

Our first dataset is from Kaggle.com.  This dataset contain "Crimes in Boston"

[Crimes in Boston](https://www.kaggle.com/ankkur13/boston-crime-data "Crimes in Boston")

Our second dataset is from data.lacity.org which has data of Crimes in LA from the year 2010 to present. 

[Crime Data from 2010 to Present- Los Angeles](https://data.lacity.org/A-Safe-City/Crime-Data-from-2010-to-Present/y8tr-7khq "Crime Data from 2010 to Present")

We decided to choose July and September of 2015 as those timeframes were common between the dataset and had adequate amount of data needed for the project.

## Transform

* Offense Code group - was not found in both the csv files so could not use it . 

* Date Occurred column - was in different format so we had to format it to the same format.

* The fields had null values so we had to do dropna to cleanup the nan values.

* The location column had latitude and longitude in the same column so we had to split the values in separate columns

* The data types of the latitude and the longitude columns were by default set to 'string' so we had to convert those columns to 'float' to create the heat map.


## Load

We decided to use SQLlite to load our transformed data, because the data retrieved from the csv files are structured. We used SQLAlchemy to interact with the SQLlite databse. The database was named as crime.db. We created "Incident_Details", "Offense_Details" and "Location_Details" to best represent the data from transformed dataset. 


#### Incident_Details:


|INCIDENT_NUMBER| OCCURRED_ON_DATE  | STREET                          | OFFENSE_CODE    |
| ------------- | ---------------   |--------------------------       | --------------- |
| I152105605	  |2015-09-01 00:00:00|	CLEVELAND PL	                  |2629             |           
| I152072583	  |2015-09-01 00:00:00|	SELDEN ST	    	                |3114             |
| I152079669	  |2015-09-01 00:00:00|	THOMAS PARK	                    |3115             |
| I162077971	  |2015-09-01 00:00:00|	COLONEL MICHAEL J. MCDONO	      |1106             |
| I162087104	  |2015-09-01 00:00:00|	FILOMENA RD		                  |1107             |


#### Offense_Details:

| offense_code  | offense_description | City        |
| ------------- | ------------------- |------------ |
| Content Cell  | Content Cell        |Content Cell |
| Content Cell  | Content Cell        |Content Cell |

#### Location_Details:

| location_num  | lat             | long         | street          | city           |
| ------------- | --------------- |------------- | --------------- | --------------- |
| Content Cell  | Content Cell    |Content Cell  | Content Cell    | Content Cell    |
| Content Cell  | Content Cell    | Content Cell | Content Cell    | Content Cell    |



## Visualize 


<img src="https://github.com/arsasvk/ETLproject/blob/Sadhana/Images/Boston-Heatmap.png" alt="Boston Heatmap" height="50%" width="50%">

<img src="https://github.com/arsasvk/ETLproject/blob/Sadhana/Images/LA%20Heatmap.png" alt="LA Heatmap" height="50%" width="50%">


### Built With

* Pandas
* Matplotlib
* SQL Alchemy
* SQLlite

### Author 

* Sadhana Kulkarni
* Meenakshi Nadimuthu


