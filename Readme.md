# Swift Logistics Analysis

## Introduction 
From an industry-wide perspective, disruptions in transportation and logistics contribute to supply chain disruptions, increased operational costs, and inefficiencies in freight movement. Whether in road, rail, air, or sea transport, delays can lead to congestion at ports and distribution hubs, increased fuel consumption, and higher carbon emissions, further impacting environmental sustainability.

Understanding the key factors contributing to disruptions is crucial for developing strategies to minimize their impact. Therefore, In today's fast-paced supply chain industry, optimizing shipment efficiency, reducing delivery times, and enhancing operational visibility are critical for success. **The goal of this project is to explore and derive actionable insights that drive decision making** for Swift logistics, featuring information on shipment records, supplier, customer and materials information, GPS tracking, vehicle information, and transportation distances.

## Strategy Implemented 🎯 

To effectively analyze the Logistics & Transportation data and provide actionable insights, I followed a systematic approach:
   1. **Business and Data understanding:** I started with making research on logistics processes, understanding the key [business questions](https://github.com/Ben-Joan/Logistics-Transportation-Analysis/blob/main/Intro%20%26%20Brief_Challenge%2024_English.docx) and Exploring the metadata and [data](https://github.com/Ben-Joan/Logistics-Transportation-Analysis/blob/main/Transportation%20%26%20Logistics%20Tracking%20Dataset.xlsx) to understand data structure and contents.
 
   2. **Data Cleaning & Transformation:** By removing duplicates and unnecessary columns e.g (Driver No), creating new columns both calculated and conditional colums, and creating a star schema model of the data. ![Image](https://github.com/Ben-Joan/Logistics-Transportation-Analysis/blob/main/ERD.PNG)

   3. **Exploratory Data Analysis (EDA):** Exploring the data, creating dax measures for key metrics and analyzing the data to answer the key business questions thereby identifying patterns and insights from the data.

   4. **Dashboard Development:** To visualize these insights effectively, I built a dynamic dashboard. The dashboard allows the monitoring of logistics performance and identifies delay causes.

   5. **Suggestions for Improvement:** Finally, based on the data analysis, I provided suggestions and strategies for reducing delay rate and optimizing efficiency.


## Insights 💡

#### Logistics Performance Overview:
**Overall Booking Performance:**
 - Total Bookings: 3,583 and Average Distance: 842 km
 - **On-Time Rate: 38.5%** (indicating a low efficiency in timely deliveries) and **Delay Rate: 61.5%** (high delay percentage, requiring investigation)
 - On average, **delivery takes: 5 days** after **7 days delay** from the planned delivery day.
 - Also, the **Lead time is averagely 9days 3hrs** (i.e the time between when the booking is made and when the order is deliverd)
 - Average **Order-to-Dispatch time** is **3hrs** indicating that most shipments starts within 24hrs of booking. 

**Booking Trends Analysis:**
 - Monthly Booking: is Peak in mid-year (June-August) and also January, but with noticeable spikes in delayed deliveries.
 - Peak booking time: 
   - Most bookings happen between 13:00 - 18:00 (1 PM - 6 PM) across all weekdays. The second busiest period is 6:00 - 12:00 (6 AM - 12 PM).Very few bookings occur between 0:00 - 5:00 AM, indicating minimal activity at night.
 - Day-wise Booking Trends:
   - Monday to Thursday show the highest volume of bookings.Friday sees a decline in bookings,
while Saturday and Sunday have the lowest bookings, with Sunday showing very little activity.

**Route, Supplier, Customer and Materials Performance:**
 - The Kanchipuram, Tamil Nadu >> Kanchipuram, Tamil Nadu route had the highest shipment volume, with low delay rate and high time efficiency, indicating proper scheduling and routing algorithm.
 - Many suppliers have significantly more delays than on-time deliveries. Top suppliers with high delays include Ekta Transport Company, Trans Cargo India, etc.
 - A significant portion of bookings across customers are delayed.Larsen & Toubro Limited and Ford India Private Limited have the highest number of bookings and very high delay rate. While Ford India has a better time efficiency, Larsen's is very low indicating that delivery is taking too long even with the less average distance being covered.
 - Auto Parts have the highest total bookings(1212) but Empty Foam and Solenoid Assembly is taking the longest time to deliver.


#### Logistics Delay Analysis: This page identifies delay analysis causes as Distance, Vehicle Type, Driver, Route and Gps provider. It shows how far shipments go and delivery time efficiency, top 10 routes where most delays occur, top 10 vehicle and driver with high delay rate and Gps provider analysis.

![Image](https://github.com/Ben-Joan/Logistics-Transportation-Analysis/blob/main/Logistics%20%26%20Transport%20Tracking_page-0002.jpg)

**Distance Analysis:**
 - Most bookings are within shorter distances (i e 0 - 500km), followed by longer distance (2000+km). But delays persist across all ranges, most occurring at the 0-500km category.
 - Delivery time increases with distance but delay does not increase at the same rate, especially at shorter distances (0-500km) which shows very poor time efficiency. Time efficiency shows the percentage of delivery time that is actually spent on transit. The very poor time efficiency at shorter distance *(11%)* indicates a severe problem which might possibly be from poor scheduling, traffic congestion or vehicle inefficiency due to high shipment volume within this distance.

**High Delay Impact:**
 - Bangalore Rural, Karnataka >> Koppal, Karnataka & Jaipur, Rajasthan>> Jhunjhunun, Rajasthan are the top route with a very high delay, especially since they're moving within short distance with small shipment.
 - 40 FT 3XL Trailer and 40FT Multi Axle Vehicles are traveling within shorter distance but have high delay rate, therefore needs to be assessed properly for better fleet management.
 - The top drivers with very high delay and poor efficiency are also identified.

**GPS Provider Analysis**
 Consent Track Gps provider being the top tracker managing more than 50% of total shipments had a very low performance in providing a routing optimization algorithm for shipments. Also, most shipments with high delay impact were managed by consent track.

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



