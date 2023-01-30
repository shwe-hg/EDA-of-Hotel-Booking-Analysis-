# EDA-of-Hotel-Booking-Analysis-
## Project Summary -

This project related to Hotel Booking Analysis having two hotel description i.e 'City Hotel' and 'Resort Hotel'.This database contains total 119390 rows and 32 columns . This data set contains booking information for a city hotel and a resort hotel, and includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things.

We divided the project in many parts those are Importing the necessary python labraries , Data collection , Data Pre Processing , EDA and Conclusion .

first step is to importing labraries i.e numpy , pandas , matplotlib.pyplot , seaborn . second step is data collection in this we find different columns which are done by using Head() , tail() ,info(),describe(),columns().

We dropped some duplicate rows by using drop() . we deleted some of null values present in the database .

In this EDA i try to come up with some questions and answered them using python topics like data wrangling , data visualization . And i have used different charts for data visualization




## Problem Statement


While booking any of the hotel the main problems we concern are about when is the best time of year to book a hotel room is? Or the optimal length of stay in order to get the best daily rate? What if you wanted to predict whether or not a hotel was likely to receive a disproportionately high number of special requests? .

These are the problems we all face , but this can be solved by a simple database of any of the hotel .


## Objective


To overcome the above problem , we are provided with a hotel bookings dataset. It will give you a brief summary of the hotel . Which can help you with the booking without any problems .


## Database


We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

1. Hotel - Name of the hotel .     

2. is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled).   

3. lead_time: number of days that elapsed between the entering date of the booking into the PMS and the arrival date.    

4. arrival_date_year: Year of arrival date .

5. arrival_date_month: month of arrival date .

6. rrival_date_week_number: week number of arrival date.

7. arrival_date_day: Day of arrival date.

8. stays_in_weekend_nights: No. of weekend nights the guest spent in a hotel.

9. stays_in_week_nights: No. of weeknights the guest spent in a hotel.

10. adults: No. of adults .

11. children: No. of children.

12. babies: No. of babies.
13. meal: Type of meal chosen.

14. country: country code.

15. market_segment: Which segment the customer belongs to.

16. distribution_channel: how thw customer accessed the stay-corporate booking/Direct/TA.TO .

17. is_repeated_guest: Guest coming for first timr or not.

18. previous_cancellations: was there a cancellation before.

19. previous_bookings_not_canceled: No. of previous bookings.

20. reserved_room_type: Room type reserved by a customer.

21. assigned_room_type: Room type assigned to the customer.

22. booking_changes: No. of changes made to booking.

23. deposit_type: Type of deposit .

24. agent: booked through a agent.

25. days_in_waiting_list: No. of days on waiting list.

26. customer_type: Type of customer.

27. required_car_parking_spaces:if car parking is required.

28. total_of_special_requests: total no. of special request.

29. reservation_status: reservation of status .

30. reservation_status_date: Date of the specific status.

. Total number of rows in database is 32
. Total number of columns in database is 119390

## Data Cleaning And Feature Engineering

1. **Removing Duplicate Rows**

All duplicate rows were dropped .

2. **Handling null values**

.Null values in columns *company* and *agent* were replaced by 0.

.Null values in column *country* were replaced by 'others'.

.Null values in column *children* were replaced by the mean of the column.


3. **Converting columns to appropriate data types**

Changed data type of *children*, *company*, *agent* to int type.

4. **Creating new columns**

.  Creating new columns *Full_stay* by adding *stays_in_weekend_nights*+ *stays_in_week_nights*

.  Creating new columns *stayed_people* by adding *adults * +*children*+*babies*.

.  Creating new columns *kids* by adding *children*+*babies*.

5. **Creating the dataframe**

. Creating the subset dataframe of *City Hotel* as *City_df*

.  Creating the subset dataframe of *Resort Hotel* as  *Resort_df*


## Exploratory Data Analysis

**Performed EDA and tried answering the following questions:**

1. What is the percentage of booking in each hotel ?
2. Which meal type is the  most preffered meal of customers?
3. What is the percentage of cancelation of booking in each hotel ?
4. What is the most preffered way of visiting hotel ?
5. What is the most preffered way of accessing the stay ?
6. How long do people stay at the hotels ?
7. Which agent makes the most no. of bookings?
8. From which country most of the guests are coming ? 
9. What is the percentage of guests require parking space ?
10. What is the Hotel wise booking of customer on the base of date , month and year ?
11. What is the variation of bookings from year to year ?
12. Which month has highest bookings ?
13. Which hotel has highest booking cancelation rate ?
14. Which time period of month has highest and lowest customers ?
15. How many customers are repeaters ?
16. Which types of customers mostly make bookings ?
17. Which room type is in most demanded by customers ?
18. what is number of stays on weekend night ?
19. what is number of stays on weekday night ?
20. what is the preferred booking type ?
21. How many special guests are there and how many special request they have made ?
















### *Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:*

                                                          

. Bar plot 



. Pie Chart 

## Univariate Analysis:

**After Performing analysis the following conclusions were made :**

1. Agent no. 9 has made most no. of bookings.
2. Most demanded room type is A and D.
3. Most popular meal type is BB(Bed and Breakfast).
4. Around 61% bookings are for City hotel and 39% bookings are for Resort hotel, therefore City Hotel is busier than Resort hotel.
5. Guests use different methods for bookings out of which most preferred way is TA/TO.
6. Surprisingly only 8% of guests need parking space .
7. Only 4% of guests visited more than once .
8. August is the most busier and profitable months for both of hotels. 
9. Most of the guests came from european countries, with highest number of guests from Portugal.
10. Most common stay length is less than 4 days and generally people prefer City hotel for short stay, but for long stays, Resort Hotel is preferred.
 

## Bivariate Analysis :

**we tried to answer some questions**

1. Almost 30 % of City Hotel bookings got canceled.where as 23% were canceled in Resort hotel .
2. There is very small percentage that customer will visit again .
3. TA/T0 is most preferred distribution channel .
4. Arrivals in hotels increases at weekends.
5. Moslty bookings are done by couples(bookings have two adults).
6. 2016 has more no of bookings as compare to other , and in every year city hotel has higher bookings than resort hotel .
7. Most guests are booking by 'No Deposit' and  most cancelation are made in 'No Deposit' . But a small amount of guest made cancelationin 'Non Refund' method. 


## Conclusion :

1. City hotel has more booking as compared to Resort hotel.
2. Most preferred food type is BB .
3. City hotel has more booking cancelation than Resort hotel.
4. Guests prefer mostly to visit as pair (2 adults).
5. Guests use different channels for making bookings out of which most preferred distribution channel is  TA/TO i.e 79.11% .
6. Maximum guests stay for less than 5 days in hotel and for longer stays Resort hotel is preferred.
7. Most of the guests came from european countries, with most of guests coming from Portugal.
8. Agent 9 has made more no of bookings than other Agents .
9. City hotel has more arrivals than Resort hotel and August have maximum bookings over a year .
10. 2016 have more arrivals than any other year .
11. 30% of bookings were canceled in City hotel .
12. Most preferred room is A & D .
13. City hotel has more bookings than Resort hotel irrespective of weekend and weekdays .
14. City hotels have more no. of special requests. Most of them ask for only 1 special request ,and very few guests made 2 requests .
