Hello Everyone,
Today I am sharing my next project on Hospitality Domain “AtliQ Hospitality Dashboard” which was displayed in Codebasics Resume Project Challenge 1. 

Overview

This Power BI Dashboard, named "AtliQ Hospitality Dsahboard" is designed to provide them insights from the historical data to the revenue team of AtliQ Grands
Data Source

Primary Data Source is provided by the Codebasics Team in CSV format along with required additional information.

Data Model

The data model consists of the following key tables:
1. fact_aggregated_bookings   - 
   -Columns: property_id, check_in_date, room_category, successful_bookings, capacity

2. fact_bookings
   - Columns: booking_id, property_id, booking_date, check_in_date, check_out_date, no_guests, room_category, booking_platform, ratings_given, booking_status, revenue_generated, revenue_realized
   
3. dim_date
   - Columns: date, mmm yy, week no, day_type

4. dim_hotels
   - Columns: property_id, property_name, category, city

5. dim_rooms
  - Columns: room_id, room_class

Data Transformation
Data Cleaning:
1. dim_date:
	- remove the column 'day_type'
	- we are deleting this because, we got a feedback from the mock dashboard review that Friday and Saturday are considered as weekends in the industry. So we delete this column and re-create day_type using calculated columns.

2. dim_rooms
	- The column names are not captured here. So select "Use First Row as Headers" option .

Calculated Columns
1.	wn: To get the week number from the corresponding date
2.	day type: Based on the feedback from stakeholder, we considered Friday and Saturday as weekend and weekdays from Sunday to Thurdsay.

Measures
	26 various measures were created based on requirement.

Visualizations

Dashboard Overview

KPI—
1.	Revenue
2.	Occupancy %
3.	Average Rating
4.	Revenue
5.	RevPAR
6.	DSRN
7.	Occupancy%
8.	ADR
9.	Realisation%
10.	(Each KPI has WOW change movement shown below it.)

 % Revenue by Category: Pie Chart showing Revenue % of each Category.
Trends by Key Metrics. Week No. trends of key metrics like RevPar, ADR, Occupancy %
Realisation % and ADR by Booking Platform: Column chart showing Realisation and ADR by various booking platforms.
Property by Key Metrics: Properties of AtliQ by various metrics shown in the form of table.


Filters and Slicers

City Slicer: Allows to select specific city
Room class Filter: Enables users to focus on a specific room type.
Status Filter: Allows to check the status of room (booked, cancelled, etc)
Year-Month Filter: selection between year-month
Week no. Filter: select week no. on selected year-month filter

Insights :
-Mumbai is the highest revenue city with 0.67bn, whereas Delhi has the least revenue of about 0.3bn.
-ADR and Realisation% diverged the most when the Booking_platform was direct offline, when ADR were 1279305.65 higher than Realisation %.
-In terms of monthly percentages, all platforms saw decreased revenue in June and gradually began to grow revenue in July on platforms "others 0.03%" ,"travel- 1.83%", and "direct online- 4.54%".
-AtliQ Excotica performs better compared to all 7 types of properties with 320 million revenue, rating- 3.62.
-Mumbai has an occupancy% of 57.8%, while delhi has a rate of 60.4%. Yet, Mumbai has the larger income of 661 million. it is because the RevPAR differs by 1057 between weekends and weekdays in Mumbai. As a result, this might have impacted to gain higher revenue.
-On a weekly basis, AtliQ Exotica and AtliQ Palace are the top income generators in Mumbai. AtliQ Bay and AtliQ City in Bangalore share up and down. AtliQ Bay is on top in Hyderabad, and AtliQ Palace is on top in Delhi. AtliQ Grand has the smallest share in any city. They must take steps to improve the ADR, rating and occupany%.


Security and Access

Dashboard Owner: Mayuri Dandekar (mayuridandekar96@gmail.com)


Feedback and Collaboration

Users are encouraged to provide feedback and suggestions. Contact for any inquiries or assistance.

Special Note:-
Really thankful to Dhaval Patel Sir for this amazing platform codebasics.io..as working on real-time datasets is of great help in understanding the data, requirements and pattern. Also Thanks to @hemanand vadival for guiding throughout the project and offcourse the stakeholder @Abhishek Anand for giving the real-world stakeholder experience during the project.




# AtliQ-hospitality-
