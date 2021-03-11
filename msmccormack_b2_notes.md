# Notes for Block 2
> Matt McCormack

## Case study: Wireless Sensor Node Data
> The first case study of block two that we are going to looking at is dealing with wireless sensor node data.
> In the discussions/block 2 portion of blackboard, our classmates posted all their questions/concerns/thoughts on this case study and how we might approach these data for our own use. Particular questions seemed to include how we will identify duplicates in some situations, when sensors turn on in relation to other sensors, 

#### Excercise 2.1: My Group (Group 3) Approach
> Group 3 (Matt McCormack, Kimya Shirazi, Conrad Ning, Keagan DeLong, Connor Sughrue, and Monica)
> * We began by creating a function to both load the data in and aggregate the data to get the arithmetic mean, based on a specified time horizon.
> ** For this, we used the read.csv function to load in each url as an R data frame, naming each with the respective last 3 digits of the time the data was from.
> * We then created a function to deal with data deduplication.
