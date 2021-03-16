# Notes for Block 2
Matt McCormack

## Case study: Wireless Sensor Node Data
The first case study of block two that we are going to looking at is dealing with wireless sensor node data.
In the discussions/block 2 portion of blackboard, our classmates posted all their questions/concerns/thoughts on this case study and how we might approach these data for our own use. Particular questions seemed to include how we will identify duplicates in some situations and when do sensors turn on in relation to other sensors.

### Excercise 2.1: My Group (Group 3)'s Approach
(Group members: Matt, Kimya, Conrad, Keagan, Connor, and Monica)
* We began by creating a function to both load the data in and aggregate the data to get the arithmetic mean, based on a specified time horizon.
** For this, we used the read.csv function to load in each url as an R data frame, naming each with the respective last 3 digits of the time the data was from.
* We then created a function to deal with data deduplication.

### Discussion Board Posts
#### Defining Duplicates
Pseudo code for defining duplicates:

read each file into a dataframe

initialize a vector of length equivalent to rows in the dataframe

iterate over rows in time column

look at each subsequent row and see if its within 7:30 minutes, if it is, add false to our vector. else, true

{
data <- read the data

vector <- c()

for (row in data){

    time_cur <- row
    
    time_next <- row+1
    
    if (time_next-time_cur>450){
    
       vector <- c(vector, FALSE)}
       
    else{
    
        vector <- c(vector, TRUE)}
}
        
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
