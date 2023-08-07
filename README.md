# EDA-Hotel-Booking-Analysis
## Objective

The objective of this project is to perform an EDA on the hotel booking dataset to gain some insights which will be helpful in understanding the patterns and trends in booking analysis, cancellation analysis, Revenue analysis, customer segmentation and competitive analysis. The valuable insights gained will be helpful in improving operational efficiency, better financial management, increasing revenue, and supporting data-driven decision-making and competitive positioning.

## Dataset

There are 119390 rows and 32 columns in this dataset.

### Variable description
1. **hotel**: Categorical - Resort hotel or city hotel.
2. **is_canceled**: ‘1’ for booking and ‘0’  not cancelled.
3. **lead_time**: Period between the time of booking and checking in (considered in days here).
4. **arrival_date_month**: Arrival month
5. **country**: Country of origin. List of 158 countries.
6. **days_in_waiting_list**: Number of waiting days.
7. **Deposit_type**: Categorical - No-deposit, Non-Refund, Refundable.
8. **Adr**: Average Daily rate as defined by the average rental revenue earned for an occupied room per day.
9. **Adults, Babies, Children**: Number of adults, babies and children.
10. **Assigned Room Type**: Code for the type of room assigned to the booking.
11. **Booking Changes**: Number of changes/amendments made to the booking from the moment the booking was entered on the PMS until the moment of check-in or cancellation.
12. **Distribution_channel**: Booking distribution channel.
13. **Is_repeated_guest’**: Categorical- repeated guest(1) or not (0).
14. **Company**: ID of the company/entity that made the booking or is responsible for paying the booking.
15. **Customer Type**: Categorical:
- Contract – when the booking has an allotment or other type of contract
associated to it
- Group – when the booking is associated with a group;
- Transient – when the bookings are not part of a group or contract, and is not associated with other transient booking;
- Transient party – when the booking is transient to at least another transient booking.
16. **Market_segment**: Market segment designation.
17. **Previous_cancellations**: Number of previous bookings that were cancelled by the customer prior to the current booking.
18. **Required_car_parking_spaces**: Number of car parking spaces required by the customer.
19. **Reservation_status**:Categorical:
- Cancelled – booking was cancelled by the customer.
- Check Out – customer has checked in but already departed.
- No Show – The customer did not check in and did inform the hotel of the reason why.
20. **Reservation_status_date**: The date at which the last status was set. This variable can be used in conjunction with the Reservation Status to understand when was the booking cancelled or when the customer checked out of the hotel.
21. **Reserved_room_type**: Code of room type reserved.
22. **Types_of_special_requests**: Number of special requests made by the customer (e.g. Twin bed or high floor)
23. **Stays_in_weekend_nights**, **Stays_in_week_nights**: Number of weekend nights and weeknights the guest stayed or booked to stay at the hotel.

## Data Wrangling

#### (1) Duplicate Rows Removal

All duplicate rows have been eliminated.

#### (2) Handling Null Values

The null values in the "company" and "agent" columns have been substituted with 0.
The null values in the "country" column have been replaced with 'others'.
The null values in the "children" column have been replaced with the mean value of the column.

#### (3) Conversion of Columns to Appropriate Data Types

The data type of the "children," "company," and "agent" columns has been changed to integer.
The data type of the "reservation_status_date" column has been converted to date.

#### (4) Eliminating Outliers

An outlier was detected in the "ADR" column and removed.

#### (5) Creation of New Columns

A new column called "total_stay" has been generated by adding the values from the "stays_in_weekend_nights" and "stays_in_week_nights" columns.
Another new column called "total_people" has been created by summing the values of "adults," "children," and "babies."


## Problem Statement

### Booking Analysis

Which type of hotel has the maximum booking?
Which agent has done a max number of bookings?
Which distribution channel leads to maximum booking?

### Know about your hotel

Which is your most preferred meal?
Which country do most guests come from??
Which is the most preferred room type?
How long do people stay at a hotel?

### Revenue Analysis

Which type of hotel seems to make more revenue?
Which room type generates the highest adr?
Which distribution channel brings better revenue-generating deals for a hotel?

### Cancellation analysis

Which type of hotel has more cancellations?
Which distribution channel has the highest cancellation?
Is there any impact of longer waiting days and lead time on cancellation?

### Time wise Analysis

To track month-on-month booking?
To track the month-on-month adr of the hotel?
To track the year-on-year booking?

### Customer retention

How-many percentage of guest has arrived again?
Which hotel has a high chance that its customer will return for another stay?

## The Solution to Business Objective

### Booking optimisation:

Strengthen partnerships with high-performing agents for increased bookings and revenue.
Improve presence and content on GDS platforms to boost bookings.
Explore collaborations with travel agencies and online platforms to expand reach.

### Revenue Management:

Increase the number of high-demand room types A and H.
Price different room types strategically to maximize revenue.
Adjust pricing strategies and revenue management techniques based on the ADR performance of each hotel.
Optimize pricing during peak and off-peak periods.
Resort Hotel need to increase outreach on GDS channel to increase revenue.

### Operations:

Optimize inventory and supply management based on most preferred meal types i.e. BB (Bread and breakfast).
Assess and optimize strategies related to TA/TO bookings.

### Cancellation Management:

Hotels to assess and optimize their strategies related to bookings made through TA/TO. By analyzing the reasons behind the high cancellation rate and addressing them, hotels can work towards reducing cancellations and improving customer satisfaction and retention.
Lead time, Number of waiting days and not getting the requested room types does not impact the cancellation. This information can help hotels focus their efforts on other potential causes of cancellations and develop strategies to reduce them.

### Customer Retention:

Focus on customer retention and loyalty programs to encourage repeat bookings and minimize cancellations.
Identify and address issues affecting customer trust and satisfaction.
For longer stay, the better deal for customer can be finalised.

### Customer Satisfaction:

Ensure guests receive requested or comparable rooms.
Train staff in foreign languages for better guest experience.
Adjust pricing and availability based on booking behavior, lead time and planning patterns.

### Marketing Strategy:

Customize marketing tactics, packages, and promotions for each hotel based on their market proportions.
Offer discounts or incentives to repeat customers.
Enhance customer loyalty and retention strategies by introducing a membership plan based on repeat percentages.
Customize marketing tactics based on favored lengths of stay.
Prioritize marketing efforts based on countries that contribute the most guests.

## Conclusion:

City hotels account for approximately 60% of the bookings, while Resort hotels comprise around 40% of the bookings.
Agent 9 has done the maximum number of bookings.
TA/TO channel has highest booking followed by corporate channel.
Bookings were very low through GDS channel.
Most preferred meal type is BB (Bed and breakfast).
Portugal and other European countries have the most guests.
Room type A is most preferred followed by D and E.
Most stays are usually shorter than 5 days, with a preference for City hotels. Conversely, for longer durations, Resort hotels are the preferred choice.
The average ADR of city hotels is slightly higher compared to resort hotels, despite resort hotels having more bookings.
Room type H generate highest revnue followed by G. Room type L generated lowest revnue.
GDS channel brings higher revenue generating deal, in contrast to that most bookings come via TA/TO.
Resort hotel has more revnue generating deals by direct and TA/TO channel. Resort Hotel need to increase outreach on GDS channel to increase revenue.
Most of the adr is below 400.
As the length of stay increases, the ADR tends to decrease.
The non-allocation of the requested room type does have an impact on the average daily rate (ADR). Generally, those who did not receive the requested room type have paid a slightly lower ADR, with only a few exceptions.
Nearly 30% of the bookings made for City Hotel were ultimately canceled.
The booking cancellation rate for TA/TO is the highest, indicating that there is a 30% likelihood of a booking made through TA/TO getting cancelled. Corporate has least cancellation percentage.
Cancellation of bookings generally occurs within 200 days of the waiting period.
The non-allocation of the requested room type, waiting days and lead time do not significantly impact the likelihood of cancellation.
Both types of hotel bookings experience an upward trend from January to August, with a minor dip in June for resort hotels. Subsequently, bookings start to decline.
The month of August demonstrates the highest demand across the observed period.
In both type of hotel, adr rises from starting of year till august and the start decreasing and then slightly increse in december.
In July and August resort hotel generates more adr than city hotel.
The "Arrival_num" exhibits small peaks at regular intervals, which could be attributed to increased arrivals on weekends. Moreover, the average daily rate (ADR) tends to increase towards the end of the month.
There are very less repeated customer.
The Resort Hotel shows a slightly higher percentage of repeat customers compared to the City Hotel.
City hotel has slightly higher median lead time. Also median lead time is significantly higher in each case, this means customers generally plan their hotel visits way to early.

 








