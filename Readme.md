# Swift Logistics Analysis

## Introduction 
From an industry-wide perspective, disruptions in transportation and logistics contribute to supply chain disruptions, increased operational costs, and inefficiencies in freight movement. Whether in road, rail, air, or sea transport, delays can lead to congestion at ports and distribution hubs, increased fuel consumption, and higher carbon emissions, further impacting environmental sustainability.

This project analyzes shipment and transportation data for Swift Logistics to identify delay drivers, performance gaps, and optimization opportunities. The goal is to generate actionable insights that support data-driven decision-making and operational improvement.

**Goal: Improve shipment efficiency, reduce delivery delays, and enhance logistics performance visibility.**

The data features information on: shipment records, supplier, customer and materials information, GPS tracking, vehicle information, and transportation distances, etc.

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
- Total Shipments: Total number of bookings processed

      Formula: COUNT(Shipment_ID)

- Average Distance: Mean distance traveled per shipment

      Formula: SUM(Distance) / Total Shipments
  
- Average Delivery Time: Average transit time per shipment

      Formula: AVG(Trip End Date − Trip Start Date)

- Average Delay: Average deviation from planned delivery date

      Formula: AVG(Actual ETA − Planned ETA)
  
- Average Lead Time: End-to-end order fulfillment duration

      Formula: AVG(Actual ETA − Booking Date)

- Order-to-Dispatch Time: Time from booking to trip start

      Formula: AVG(Trip Start Date − Booking Date)

- On-Time Delivery Rate: Percentage of on-time shipments

      Formula: (On-Time Shipments ÷ Total Shipments) × 100

- Delay Rate: Percentage of delayed shipments

      Formula: (Delayed Shipments ÷ Total Shipments) × 100


## Insights 💡

#### Logistics Performance Overview:
**Overall Booking Performance:**
 - **Total Bookings: 3,583** and **Average Distance: 842 km**
 - **On-Time Rate: 38.5%** (indicating a low efficiency in timely deliveries) and **Delay Rate: 61.5%** indicating significant delivery inefficiencies.
 - Average delivery occurs **5 days after dispatch**, with an **average 7-days delay** beyond planned ETA
 - The **Lead time** is averagely **9 days** (i.e the time between when the booking is made and when the order is delivered)
 - Average **Order-to-Dispatch time** is **~3hrs** indicating fast shipment initiation after booking.

**Booking Trends Analysis:**
 - Seasonality: Peak bookings occur in **January and mid-year (June–August)**, with January showing a notable spike in delays.
 - Time of day: Most bookings occur between **09:00 and 18:00**, aligning with business operating hours
 - Day of week:
      - Highest booking volumes from **Monday to Thursday**
      - Decline on **Fridays**, with minimal activity on weekends
    
**Route, Supplier, Customer and Materials Performance:**
 - High-volume state routes: **Tamil Nadu >> Tamil Nadu, Maharashtra >> Tamil Nadu & Tamil Nadu >> Maharashtra**
 - High-volume city routes: **Kanchipuram >> Kanchipuram, Gurgaon >> Kanchipuram & Pune >> Kanchipuram**
 - **Geographic concentration**: Tamil Nadu, particularly Kanchipuram, is a major shipment hub
 - Most high-volume routes experience **high delay rates**, especially those exceeding **500 km**
 - **Supplier performance:**
      - Several suppliers have more delayed than on-time deliveries. Top **high-delay suppliers** include Unknown, Ekta Transport Company, and Trans Cargo India.
 - **Customer performance:**
      - **Larsen & Toubro Limited and Ford India Private Limited** have the highest shipment volumes and high delay rate.
 - **Material movement:**
      - Auto Parts have the highest shipment volume, Empty Foam and Solenoid Assembly experience the longest delivery times
 - **GPS Provider Performance**
      - Consent Track GPS manages over 50% of shipments
      - Despite high usage, it shows poor route visibility and tracking performance. A large share of highly delayed shipments are associated with this GPS provider, limiting real-time monitoring and delay mitigation.


## Dashboard View
![Dashboard1](https://github.com/Ben-Joan/Swift-Logistics/blob/main/Images/Overview.PNG)

![Dashboard2](https://github.com/Ben-Joan/Swift-Logistics/blob/main/Images/Time.PNG)

![Dashboard3](https://github.com/Ben-Joan/Swift-Logistics/blob/main/Images/Delay.PNG)

[Explore the Dashboard](https://app.powerbi.com/view?r=eyJrIjoiODFkNzlhYTQtYmE4NC00ODI2LTlkMDUtNGFjOTQ5N2Q5OTdmIiwidCI6IjczMDc4ZWNkLWYzM2UtNDQxYy05ODYyLWVhZDdjNjFhNGU4MiJ9)


## Recommendations 🚀
To improve transportation efficiency:

1. **Improve On-Time Delivery Performance**: Establish SLA-based performance targets for routes exceeding 500 km, Prioritize delay reduction initiatives on high-volume and high-delay routes

2. Route & Network Optimization: Reevaluate long-distance routes for consolidation or alternative routing, Introduce route-level performance benchmarking to identify chronic bottlenecks

3. **Supplier & Carrier Management**: Conduct supplier performance audits for high-delay carriers, Introduce incentive-based contracts tied to on-time delivery metrics and Reduce reliance on “Unknown” suppliers to improve accountability.

4. GPS & Visibility Enhancement

Reassess partnership with Consent Track GPS

Improve tracking accuracy and real-time visibility to enable proactive delay management

Consider multi-provider GPS redundancy for high-value or time-critical shipments

5. Demand & Capacity Planning

Strengthen capacity planning for January and mid-year peaks

Align staffing and fleet availability with weekday demand patterns

6. Material-Specific Process Improvements

Investigate handling and packaging processes for Empty Foam and Solenoid Assembly

Introduce material-specific lead time benchmarks and monitoring

By implementing these recommendations, there will be improvement in transportation efficiency, reducing delays, and enhancing customer satisfaction.





