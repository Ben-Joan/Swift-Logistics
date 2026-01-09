# Swift Logistics Analysis

## Introduction 
From an industry-wide perspective, disruptions in transportation and logistics contribute to supply chain disruptions, increased operational costs, and inefficiencies in freight movement. Whether in road, rail, air, or sea transport, delays can lead to congestion at ports and distribution hubs, increased fuel consumption, and higher carbon emissions, further impacting environmental sustainability.

Understanding the key factors contributing to disruptions is crucial for developing strategies to minimize their impact. Therefore, In today's fast-paced supply chain industry, optimizing shipment efficiency, reducing delivery times, and enhancing operational visibility are critical for success. 
**The goal of this project is to explore and derive actionable insights that drive decision making and Operational improvemt for Swift logistics**

Available data features information on shipment records, supplier, customer and materials information, GPS tracking, vehicle information, and transportation distances, etc.

## Key Questions 

To effectively analyze the Logistics & Transportation data and provide actionable insights:
   1. Top Routes: What are the most common shipment routes and their average distances?
   2. Delivery Times: Which routes have the longest delivery times?
   3. Peak Shipments: When are the busiest booking and delivery dates?
   4. Delays Analysis: What factors contribute to shipment delays?
   5. Supplier Trends: Which suppliers handle the most shipments, and do some have higher delays?
   6. Customer Insights: Which customers receive the most shipments, and do they experience delays?
   7. Material Movement: What are the most frequently shipped materials, and do certain materials have longer delivery times?
   8. Bottlenecks: Where are the most common shipment delays based on GPS data?
   9. Route Optimization: What strategies can improve transportation efficiency?
       
### Measured KPIs Include:
- Total Bookings (Shipments)
- Average Distance
- Average Delivery: Time between trip start date and trip end date
- Average Delay: Time difference between Actual ETA and Planned ETA
- Average Lead Time: Time between booking date and Actual ETA i.e when delivered
- Order-to-Dispatch: Time between when Shipment was booked and when trip started
- Ontime Delivery Rate
- Delay Rate

## Insights 💡

#### Logistics Performance Overview:
**Overall Booking Performance:**
 - **Total Bookings: 3,583** and **Average Distance: 842 km**
 - **On-Time Rate: 38.5%** (indicating a low efficiency in timely deliveries) and **Delay Rate: 61.5%** (high delay percentage, requiring investigation for reduction)
 - On average, **delivery takes: 5 days** after **7 days delay** from the planned delivery day.
 - The **Lead time** is averagely **9 days** (i.e the time between when the booking is made and when the order is delivered)
 - Average **Order-to-Dispatch time** is **3hrs** indicating that most shipments starts less than 24hrs of booking. 

**Booking Trends Analysis:**
 - Monthly Booking: is Peak in **mid-year (June-August) and also January**, but with noticeable spikes in delayed deliveries especially January.
 - Peak booking time: 
   - Most bookings happen between **09:00 - 18:00 (9 AM - 6 PM) across all weekdays**, which is official workhours while fewer bookings occur at other time of the day.
 - Day-wise Booking Trends:
   - **Monday to Thursday** show the highest volume of bookings. Friday, sees a decline in bokings and also during the weekend, indicating minimal activity on these days.
   - 
**Route, Supplier, Customer and Materials Performance:**
 - State Level: **Tamil Nadu >> Tamil Nadu, Maharashtra >> Tamil Nadu & Tamil Nadu >> Maharashtra** route had the highest shipment volume
 - City Level: **Kanchipuram >> Kanchipuram, Gurgaon >> Kanchipuram & Pune >> Kanchipuram** route is the top shipment route.
 - That is Tamil Nadu State is where most shipments is either coming from or going to and Kanchipuram is the top city for to-and-fro shipments.
 - Also majority of the routes (both state and city), experiencing high delay rate travel > 500KM distance.
 - Many suppliers have significantly more delays than on-time deliveries. Top suppliers with high delays include **Unknown, Ekta Transport Company, Trans Cargo India,** as the top 3.
 - A significant portion of bookings across customers are delayed. **Larsen & Toubro Limited and Ford India Private Limited** have the highest number of bookings and very high delay rate.
 - Auto Parts have the highest total bookings (1212), but **Empty Foam and Solenoid Assembly** is taking the longest time to deliver.

**GPS Provider Analysis**
 Consent Track Gps provider being the top tracker managing more than 50% of total shipments had a very low performance in providing a route for shipments. Most shipments, especially those with very high delay rate was managed by consent track.


## Dashboard View
![Dashboard1](https://github.com/Ben-Joan/Swift-Logistics/blob/main/Images/Overview.PNG)

![Dashboard2](https://github.com/Ben-Joan/Swift-Logistics/blob/main/Images/Time.PNG)

![Dashboard3](https://github.com/Ben-Joan/Swift-Logistics/blob/main/Images/Delay.PNG)

[Explore the Dashboard](https://app.powerbi.com/view?r=eyJrIjoiODFkNzlhYTQtYmE4NC00ODI2LTlkMDUtNGFjOTQ5N2Q5OTdmIiwidCI6IjczMDc4ZWNkLWYzM2UtNDQxYy05ODYyLWVhZDdjNjFhNGU4MiJ9)


## Recommendations 🛠️
To improve transportation efficiency:

 - **Improve Scheduling and Resource Allocation:** Delivery time efficiency analysis reveals poor efficiency for shorter distances, indicating potential issues with scheduling, slow processing times, or ineffective last-mile delivery strategies. To address this, allocating additional resources such as vehicles and drivers can help optimize booking schedules and delivery operations. Thereby, enhancing overall delivery time efficiency.


 - **Switch to More Reliable GPS Providers:** Review Consent Track System or consider replacing with more reliable trackers like Vamosy, Apace Transco, or a combination of Vamosy with Ekta or Krc Logistics for better route optimization and tracking.

 - **Supplier and Customer Relationship Management:** Investigate top suppliers with high delay rates and prioritize top customers with long delivery time (e.g., Larsen, Otis Elevator) to maintain business relationships

 -  Ensure adequate resources and staffing during peak periods i.e mid-year, weekdays, 1-6 pm to avoid delayed schedule and drivers for delivery.

 - **Vehicle Maintenance:** Further Investigation of the vehicles with high delay impact and perform necessary maintenance to prevent unnecessary breakdowns.

By implementing these recommendations, there will be improvement in transportation efficiency, reducing delays, and enhancing customer satisfaction.




