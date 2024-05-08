## Cyclistic Power BI Dashboard

<a href="https://app.powerbi.com/links/EVlY7EUaXW?ctid=e14e73eb-5251-4388-8d67-8f9f2e2d5a46&pbi_source=linkShare">Access My Dashboard from here!</a>

### Introduction:
The Cyclistic Power BI Dashboard project is a comprehensive data analysis and visualization initiative undertaken as part of the Google Data Analytics Capstone project. The project aims to transform raw Cyclistic bike-share data into actionable insights through interactive and visually engaging dashboards.

### Project Steps:

1. **Data Transformation**: 
   - The project begins with data acquisition and transformation. Raw data is imported into Power BI and transformed to ensure consistency and usability.
   - Column values are standardized by replacing values such as "classic_bike" with "Classic Bike" using the "Replace Values" transformation feature.
   - Additional columns are created to extract meaningful information, including month names, month numbers, quarters, and weekday numbers. This ensures proper ordering of months and weekdays for visualization purposes.

2. **Data Modeling and Measures**:
   - Key performance indicators (KPIs) are defined, such as total monthly rides and average monthly ride length.
   - Measures are created using Data Analysis Expressions (DAX) to calculate metrics such as average ride length and total rides for different user types and bike categories.

   ```DAX
   Average_rideLength_casual = 
       CALCULATE(
           AVERAGE(merged_data[Ride_length_in_mins]),
           FILTER(merged_data, merged_data[member_casual] = "Casual")
       )

   Total_rides_casual = 
       CALCULATE(
           COUNT(merged_data[ride_id]),
           FILTER(merged_data, merged_data[member_casual] = "Casual")
       )
   ```

3. **Visualization Creation**:
   - Various visualizations are developed to provide insights into bike-share usage patterns.
   - Clustered bar charts depict total rides by bike type, while clustered column charts showcase average ride length by bike type.
   - Line charts visualize trends in total quarterly rides, total daily rides, quarterly average ride length, and daily average ride length.

4. **Dashboard Development**:
   - Three distinct dashboards are created: a general overview, total rides analysis, and average ride length analysis.
   - Each dashboard offers specific insights and facilitates easy navigation between different sections, enhancing user experience and understanding.

5. **Interactivity and Navigation**:
   - Navigation buttons are integrated to enable seamless navigation between dashboards, allowing users to explore various analyses and insights effortlessly.

### Project Outcome:
The Cyclistic Power BI Dashboard project demonstrates advanced skills in data manipulation, transformation, visualization, and dashboard development. By leveraging Power BI's capabilities, the project transforms complex bike-share data into actionable insights, providing stakeholders with valuable information to optimize bike-share operations and improve user experience.
