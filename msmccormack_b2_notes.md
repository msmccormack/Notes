# Notes for Block 2
Matt McCormack

## Case study 1: Wireless Sensor Node Data
The first case study of block two that we are going to looking at is dealing with wireless sensor node data.
In the discussions/block 2 portion of blackboard, our classmates posted all their questions/concerns/thoughts on this case study and how we might approach these data for our own use. Particular questions seemed to include how we will identify duplicates in some situations and when do sensors turn on in relation to other sensors.

### Discussion Board Posts for Case Study 1:
#### Defining Duplicates
Pseudo code for defining duplicates:

read each file into a dataframe

initialize a vector of length equivalent to rows in the dataframe

iterate over rows in time column

look at each subsequent row and see if its within 7:30 minutes, if it is, add false to our vector. else, true


    data <- read the data

    vector <- c()

    for (row in data){

        time_cur <- row
    
        time_next <- row+1
    
        if (time_next-time_cur<450){
    
           vector <- c(vector, FALSE)}
       
        else{
    
           vector <- c(vector, TRUE)}
        
#### The Game Plan
1) Read in all the data
2) Filter each dataframe for duplicates
3) Merge the data together
4) Sort by time
5) Aggregate
6) Create figures

#### Temporal Data
1) Maybe create vectors of numbers to represent month, day, hour, minute, second (pros: numeric, easy to aggregate, easy to filter with) rather than using strings
2) Look for an R package that processes the date and time data we have for ease of comparison


### Excercise 2.1: My Group (Group 3)'s Approach
(Group members: Matt, Kimya, Conrad, Keagan, Connor, and Monica)
* We began by creating a function to both load the data in and aggregate the data to get the arithmetic mean, based on a specified time horizon.
** For this, we used the read.csv function to load in each url as an R data frame, naming each with the respective last 3 digits of the time the data was from.
* We then created a function to deal with data deduplication. The code for this is as follows:

## Case Study 2: Working with FLUXNET Tower Data
The second case study looked into FLUXNET tower data. This data consists of a network of towers that measure energy and gas fluctuations between the Earth's surface and the atmosphere. There are times when sensors malfunction, operations are interupted, or other factors that cause gaps in the datasets. Our goal with this case study is to figure out how to reconstruct missing data. 

### Gap Filling
In case study 2, we end up with large gaps in the discrete time series. Every half an hour, we should have an observation; however, there are clearly lots of gaps. How do we fill in the gaps?
* How do we model radiation?
** Modelling radiation depends a lot about time. 

### Discussion Board Posts for Case Study 1:

####

### Exercise 2.2: My Group's Approach
