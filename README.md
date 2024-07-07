#Problem Statement:- ITC Hotels aims to enhance its revenue and overall profit percentage, addressing challenges that are impacting financial performance.

#Data transformation:- 
In the #Bookings tables Stay Nights, Rev per night, Revenue Realized, Refund and Days prior Check-in are calculated. 
Those who have booked between 0-2 days before check-in are considered Urgent.
Those who have booked between 3-7 days before check-in are considered Few Days.
Those who have booked more than 7 days before check-in are considered More Days.
For the Ratings Column, the values of Cancelled and No-Show Booking Status are kept null while for the checked-out null values we have filled the Average Rating of that particular property ID.
Created a new #table named #Cancellation where we have calculated the total no. of cancellations based on property ID, Room ID, and Date. This is further used to calculate the occupancy and total successful bookings (Checked-Out + No-show).
In the #Date table Week number of year, Day name, and assigning day type (Weekday and Weekend). In Hotel Industry Friday and Saturday are considered as Weekends.
#Data Modelling:- 
Modeled the data based on one-to-many relationships using property ID, date, room ID, and Room class.
#Key Measures:-
#Average Daily Rate (ADR):- ADR is a key performance metric in the hospitality industry that measures the average revenue earned per occupied room over a specific period. It is calculated by dividing the total room revenue by the number of rooms sold (occupied rooms).
The formula is:
#ADR = ([Revenue Realized]/([Total Successful Bookings]+([Cancelled]*0.4)))
We have taken 40% of the canceled amount only because we have refunded the rest amount.
#Revenue Per Available Room (RevPar):- It measures the revenue generated per available room, regardless of whether the room is occupied or not. It provides a comprehensive picture of a hotel's financial performance.
The formula for RevPAR is:
#RevPAR = Revenue Realized/ Number of Available Rooms
Alternatively, it can also be calculated by multiplying the ADR (Average Daily Rate) by the Occupancy Rate:
RevPAR = ADR×Occupancy Rate

#Conclusion:- 
There is a large number of cancellations coming from customers staying for 1 and 2 nights and booking rooms immediately. 
Also, revenue and Occupancy for Weekends and Weekdays are almost equal which shows that the per-day demand for weekdays is much less than that for weekends.
#Solution:- 
For Urgent Bookings refund should not be given
For the Few Days before booking refund amount should be 40% of the total room rent.
For the More Days before bookings refund can be kept as it is.
For Weekdays hotels can start giving offers like Gala Dinner, Live Music, Membership cards, and Cultural activities.






