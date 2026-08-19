Logistics Performance Dashboard – Power BI
Project Overview

This project presents an interactive Logistics Performance Dashboard developed using Microsoft Power BI. The dashboard analyzes transportation and delivery operations using trip-level data, including Trip ID, Vehicle ID, Driver ID, Origin, Destination, Distance Travelled, Fuel Consumed, Delivery Status, and Delivery Date.

The purpose of the project is to monitor logistics performance, analyze delivery efficiency, evaluate vehicle and driver activity, and identify transportation patterns through interactive visualizations.

Dataset

The dataset contains the following key fields:

Trip_ID – Unique identifier for each trip
Vehicle_ID – Vehicle assigned to the trip
Driver_ID – Driver responsible for the trip
Origin – Starting location
Destination – Delivery destination
Distance_km – Distance travelled in kilometres
Fuel_Consumed_L – Fuel consumed in litres
Delivery_Status – On-Time or Late delivery
Delivery_Date – Date of delivery

For example, the dataset contains routes such as Delhi–Pune, Mumbai–Bangalore, Mumbai–Pune, and Hyderabad–Pune.

Data Cleaning and Transformation

The dataset was cleaned and transformed using Power Query Editor before creating the dashboard.

The main data-cleaning steps included:

Removing blank rows
Assigning appropriate data types
Trimming and cleaning text columns
Checking duplicate Trip IDs
Standardizing delivery-status values
Handling missing fuel-consumption values
Converting Delivery Date to Date format
Creating Year and Month fields for time-based analysis

Some records contain missing fuel-consumption values, so these were considered when performing fuel-related analysis.

DAX Measures

The following measures were created to calculate important logistics KPIs:

Total Trips =
DISTINCTCOUNT(Trips[Trip_ID])


Total Distance =
SUM(Trips[Distance_km])


Total Fuel =
SUM(Trips[Fuel_Consumed_L])


Fuel Efficiency =
DIVIDE(
    [Total Distance],
    [Total Fuel],
    0
)
Dashboard Visualizations

The Power BI dashboard includes:

KPI Cards
Total Trips
Total Distance Travelled
Total Fuel Consumed
Fuel Efficiency
Donut Chart – Delivery Status
Compares On-Time and Late deliveries.
Clustered Column Chart – Distance by Vehicle
Compares the total distance travelled by each vehicle.
Bar Chart – Trips by Driver
Shows the number of trips completed by each driver.
Line Chart – Delivery Trend
Displays trip activity over time based on delivery dates.
Origin-to-Destination Matrix
Analyzes the number of trips between different origins and destinations.
Interactive Slicers
Vehicle ID
Driver ID
Delivery Status
Delivery Date
Dashboard Objective

The primary objective of this dashboard is to provide a clear and interactive overview of logistics operations. It helps users evaluate delivery performance, vehicle utilization, driver activity, fuel consumption, travel distance, and route patterns.

The dashboard can support operational decision-making by making logistics performance easier to monitor and analyze.

Tools Used
Microsoft Power BI Desktop
Power Query – Data cleaning and transformation
DAX – Measures and KPI calculations
Power BI Visualizations – Dashboard development
Conclusion

The Logistics Performance Dashboard converts raw transportation data into meaningful and interactive business insights. It demonstrates the use of data cleaning, data transformation, DAX calculations, data visualization, and dashboard design in Power BI.
