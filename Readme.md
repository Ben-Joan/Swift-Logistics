# Swift Logistics Analysis

## Executive Summary

This project analyzes shipment and transportation data for Swift Logistics to **identify the root causes of delivery delays and inefficiencies** across routes, suppliers, customers, and materials. Using operational KPIs such as on-time delivery rate, lead time, and delay duration, the analysis reveals that **over 60% of shipments are delayed**, with **long-distance routes (>500 km), supplier performance gaps, and limited GPS visibility** as the primary contributors. The findings provide data-backed recommendations for route optimization, supplier accountability, capacity planning, and tracking improvements to enhance delivery reliability, reduce lead times, and support more efficient logistics operations.

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

1. **Improve On-Time Delivery Performance**: Since more than 60% of shipments are delayed, Swift Logistics should focus on improving delivery timing.
Set clear delivery targets for long-distance routes (especially routes above 500 km) where delays are most common. Regularly track delivery performance
to quickly identify routes that need attention.

2. **Optimize Routes and Transportation Planning:** Review frequently used long-distance routes to see if better or shorter alternatives are available.
Combine shipments where possible to reduce repeated trips on the same route. Monitor routes that consistently experience delays and prioritize them for improvement.

3. **Strengthen Supplier and Carrier Performance:** Evaluate suppliers and transport partners that record more delays than on-time deliveries. Work more
closely with reliable suppliers and reduce dependency on poorly performing or unidentified (“Unknown”) carriers.Introduce simple performance tracking so
suppliers understand where they need to improve.

4. **Improve Shipment Tracking and Visibility:** Since Consent Track GPS manages most shipments but shows weak performance, Swift Logistics should review
its effectiveness. Improve GPS tracking to allow better visibility of shipment locations and delays. More reliable tracking will help operations teams
respond faster when issues occur during transit

5. **Plan Better for Peak Periods:** Increase planning and resources during January and mid-year (June–August) when shipment volume is highest.
Ensure enough vehicles, drivers, and support staff are available during busy periods. Better planning during peak times will reduce pressure on the system
and limit delays.

6. **Address Material-Specific Delays:** Investigate why Empty Foam and Solenoid Assembly shipments take longer to deliver. Review handling, packaging, and transportation methods for these materials. Set realistic delivery timelines for materials that require special handling.

By implementing these recommendations, there will be improvement in transportation efficiency, reducing delays, and enhancing customer satisfaction.



