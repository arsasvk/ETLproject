# ETLproject - TECHNICAL REPORT- Crime Data Analysis

## Introduction

We analysed the crime data for two large US cities, namely Boston, Los Angeles. For the scope of this project, we concentrated on July and September 2015 data. We took two datasets from two different sources mentioned below and transformed them to create the dataframes about the Incident Details, Offense Details and the Location Details. We loaded the analysed data into the sqlite database.  
Loaded table data is used to Visualize such as "To find out the top types of offenses" , "Heat map of where the crimes happened in respective cities". 

### Extract 

Our first dataset is from Kaggle.com.  This dataset contain "Crimes in Boston"
[Crimes in Boston](https://www.kaggle.com/ankkur13/boston-crime-data "Crimes in Boston")

Our second dataset is from data.lacity.org which has data of Crimes in LA from the year 2010 to present. 

[Crime Data from 2010 to Present- Los Angeles](https://data.lacity.org/A-Safe-City/Crime-Data-from-2010-to-Present/y8tr-7khq "Crime Data from 2010 to Present")

We decided to choose July and September of 2015 as those timeframes were common between the dataset and had adequate amount of data needed for the project.

### Transform

* Offense Code group - was not found in both the csv files so could not use it . 

* Date Occurred column - was in different format so we had to format it to the same format.

* The fields had null values so we had to do dropna to cleanup the nan values.

* The location column had latitude and longitude in the same column so we had to split the values in separate columns

* The data types of the latitude and the longitude columns were by default set to 'string' so we had to convert those columns to 'float' to create the heat map.


### Load

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

#### Incident_Details:


| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  | 

#### Offense_Details:

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

#### Location_Details:

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

### Visualize 


<img src="https://github.com/arsasvk/ETLproject/blob/master/Images/Screen%20Shot%202019-05-09%20at%206.47.40%20PM.png" alt="Crime and Frequency" height="50%" width="50%">

<img src="https://github.com/arsasvk/ETLproject/blob/master/Images/Screen%20Shot%202019-05-09%20at%206.49.01%20PM.png" alt="Offense in the month of July 2015" height="50%" width="50%">


### Built With

* Pandas
* Matplotlib
* SQL Alchemy
* SQLlite

### Author 

* Sadhana Kulkarni
* Meenakshi Nadimuthu


