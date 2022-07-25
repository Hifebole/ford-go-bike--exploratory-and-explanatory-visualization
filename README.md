# (Ford GoBike System Data)



## Dataset

> This data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area.

The dataset has 183412 rows and 16 columns
 * duration_sec 
 * start_time  
 * end_time  
 * start_station_id  
 * start_station_name       
 * start_station_latitude  
 * start_station_longitude 
 * end_station_id  
 * end_station_name     
 * end_station_latitude  
 * end_station_longitude 
 * bike_id                  
 * user_type                
 * member_birth_year 
 * member_gender            
 * bike_share_for_all_trip 

 ### Objective
 The goal is to draw insights from this dataset using the variables at hand 

 ### Preliminary Data Wrangling
 Some of these preliminary data wrangling involved
 * Dropping all rows that have null values
 * Dropping columns start_station_id, start_station_latitude, start_station_longitude and the the coresponding end station columns 
 * Changed the datatypes of some columns like 
 1. bike_id (from int to string object)  
 2. member_gender, bike_share_for_all_trip and user_type (from string object to categorical datatype)

 ### During Analysis
 * I created a column for age group of the various users using their age 
  - Age groups 21 to 35 as Young Adult
  - 35 to 60 as Middle age adults
  - 60 to 80 as Senior adults



## Summary of Findings

### Univariate Exploration
* With the aid of bar chart I was able to illustrate the following
- The male gender is the dorminant group in terms of numbers followed by the female and then others
- There are a lot more Subscribers than there are Customers in this dataset
- Users that don't use bike share for all trips far outnumber those that do

* Using a histogram and also cutting out outliers in the member_age column, 
- I was able to identify the mode of the ages of users in the dataset as between the ages 25 to 35
- After rescaling (using the log scale) and cutting away outliers, The mode of the distribution of the ride durations in seconds fell between 400 seconds and 650 seconds. 

* After creating age groups , the most frequent age group is the young adult , with the senior adults being the lowest in terms of sheer counts. This will make it into my Explanatory Presentation

### Bivariate Exploration
* After Rescaling duration in seconds and plottinng it against the ages of the users using a scatterplot , the range of ride durations decreased with increase in users age

* Plotted the average durartion of rides in seconds against 
- member_gender; others edged the others out with the female gender coming in second place
- bike_share_for_all_trip; there appeared to be no significant difference
- user_type; Customers have higher average ride duration than subscriber
- age_range; Seniors have the highest average ride duration 

* I then visualised this same relationship but this using boxplot to give a better insights on what is going on

### Multivariate Exploration
* Using Clustered bars chart I created a plot with the variables duration_sec, age_range and gender, the visual followed the trend we had been seeing except with the "other" gender type, where the young adult were having higher average ride duration in seconds than that of senior adults , this was later clearified with another cluster bar that showed that there was a significant amount of difference between the other gender class in the young adult and that of the senior adults
* A boxplot to clarify and further butress the point that the senior adults have higher average ride duration about the above relationship (this would feature in my explanatory analysis)
* Finally another clustered bar chart to show the relationship between average ride duration, user type and age group 


## Key Insights for Presentation

* The major trend and insight is that Senior Adults from the ages 60 upwards have higher average ride durations than any other age group , this could be as a result of having more time for biking as retirees or slow riding speed 

* The amount of males in the dataset far outweighs the other genders

The subscribers have significantly lower average ride durations than customers.