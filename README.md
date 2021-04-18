# ** PyBer_Analysis

## *Project Overview*
pyBer is a ride share App. company, I was asked to analyze all the rideshare data from January to early May of 2019  and create visualizations to tell a compelling story about the data and trends. 
 To create a compelling visualization, I will write python scripts using Pandas, Jupyter, and Matplot lib to create a variety of charts to create a ride-sharing summary DataFrame by city type & a multiple-line chart of total fares for each city type.  
 
                  
## *Analysis & Results*
### Analysis
For this analysis, I will get the Ride Data CSV file that includes The city Name, Ride Date, Fare & ride ID. as well I will get the "City Table" that Includes the City Name, # of Drivers per City, and City Type.  I will use these Tables to create the end product 1) A ride-sharing summary DataFrame by city type & 2: A multiple-line chart of total fares for each city type. I will follow the below steps to get to the final product. 

1) 1st step in the analysis process is importing the relevant libraries and setting all dependencies in order to read the CSV file and be to create the Data Frame that we will use for the analysis. 

![image1](https://user-images.githubusercontent.com/80013773/115135410-1f77f780-9fcd-11eb-87ec-f7cb682c6605.PNG)

 2) Once we created the Merged DF, we will calculate the following total rides, total Drivers, total Fares per City Type. and then we will calculate the Average Fare per ride and Average fare per Driver per City.  this will be done through using count or Sum functions and Groupby on "City Type". 
 
 ![image2](https://user-images.githubusercontent.com/80013773/115135431-3fa7b680-9fcd-11eb-8149-4be75637afdb.PNG)
 
3)  Next, Using Pandas we will create the summary table (as Data Frame) for ride-sharing by city. after we create the Basic summary table we will perform formatting for the table to make sure it's clean and tell a compelling story. 

![image3](https://user-images.githubusercontent.com/80013773/115135441-4f26ff80-9fcd-11eb-8b85-e1c91c21a23b.PNG)

4) in order to create a multiple line plot that shows the total weekly fares for each type of city, I need to:
 4.1 To create a new DataFrame showing the sum of the fares for each date ( using group by function) where the indexes are the city type and date. and then Reset the Index to        convert the Type to  Series in the DataFarme
    ![image4](https://user-images.githubusercontent.com/80013773/115135452-61a13900-9fcd-11eb-9d6d-49bf0a3c4236.PNG)
       
 4.2 Then I will Create a pivot table with the 'date' as the index, the columns =' type', and values='fare' to get the total fares for each type of city by the date. and reset       the Index again. 
   ![image5](https://user-images.githubusercontent.com/80013773/115135468-84335200-9fcd-11eb-8b1c-4485a8b8bc70.PNG)

5) Last step is to plot A multiple-line chart of total fares for each city. we will Use the object-oriented interface method to plot the resample DataFrame using the df.plot() function. 

 ![image6](https://user-images.githubusercontent.com/80013773/115135475-97462200-9fcd-11eb-88a7-6370710ff1e2.PNG)
         
### Results
1) from ride-sharing summary DataFrame by city type (Table_1 below), we conclude the following: as cities get more populated, we see an exponential increase in Total # of rides, Total # of Drivers & Total Fares. But this increase led to a significant drop in Average Fare per Driver and Average Fare per Ride. resulting in less revenue per Average Driver 
  1.1 Total Rides in Urban Cities is 2.6 X total rides in Suburban cities and 13X Total rides in rural Cities. Total Rides in Suburban cities is 5X vs. Rural Cities. 
  1.2 Total # of drivers increase significantly in Urban cities is ~31X (2405 Drivers)  vs. Rural cities ( 78 Drivers). Suburban cities Total drivers is ~6X vs. rural Cities.
  1.3 Total fares, didn't increase in the same ratio as total Drivers and Total Rides. in Urban cities the increase is only 9.2X vs. Rural cities and 2X vs. Suburban cities...
  1.4.  Average Fare Ride and Average Fare per Driver Dropped significantly, leading to the conclusion as cities get more populated # of drivers increases significantly, leading to more competition and an accelerated decrease in Fares and revenue per Driver.  

  ![summary table](https://user-images.githubusercontent.com/80013773/115135558-44209f00-9fce-11eb-8410-31a3a0a4d010.png)

2) Based on "Total Fare By City Type" (see chart below), we can conclude that:
  2.1 Total fares are not stable, and they fluctuate over time, within a minor uptrend. there is some level of correlation in trend between the 3 city types.  
  2.2 Urban Fare by City type is in run-rate of ~2000 to 2500 ( with two exception points) 
  2.3 Suburan Total Fare by City Type is in run-rate ~850 to ~1400 (with few outlier points) 
  2.4 Total Fare in Rural Cities in the run-rate of ~ 50 to 500.
 
 ![Challenge_fare_summary](https://user-images.githubusercontent.com/80013773/115135490-b5138700-9fcd-11eb-891b-5374179d3999.png)

    
## *Summary*
### Advantages
 Using Python scripts using Pandas, Jupyter, and Matplot lib is a powerful tool for Data Analysis and Data visualization. It's useful for reading CSV files, performing required Data manipulation to perform the Data analysis, and then create compelling summary tables and visual Charts that convey a clear message to stakeholders and customers.
