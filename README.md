<!-- Introduction -->

# Charge Point Utilization
Denison University is committed to addressing climate change and recognizes the impact of vehicle operations on its carbon footprint. To align with sustainability goals, the university is establishing an electric vehicle (EV) charging infrastructure on campus, encouraging EV adoption. Challenges, such as charging time and network expansion, need to be addressed. Therefore, we, the DA301 "Charged" team, are committed to generating crucial insights that inform strategic decisions. Our primary objective is to provide the Campus Sustainability Committee with a comprehensive five-year plan outlining the effective implementation of electric vehicle (EV) chargers across Denison University's campus. This will be achieved through in-depth analyses of charger usage patterns, the identification of peak demand times, and the provision of recommendations aimed at enhancing usage efficiency.
<a name="readme-top"></a>
<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Motivation">Motivation</a></li>
    <li><a href="#Authors">Authors</a></li>
    <li><a href="#BuildStatus">Build Status</a></li>
    <li><a href="#Requirements">Requirements</a></li>
    <li><a href="#CodeFiles">Code Files</a></li>
    <li><a href="#DataFiles">Data Files</a></li>
    <li><a href="#Illustrations">Illustrations</a></li>
    <li><a href="#HowToUse">How To Use</a></li>
    <li><a href="#Contribute">Contribute</a></li>
    <li><a href="#Credits">Credit</a></li>
  </ol>
</details>

### Motivation
Our primary motivation is to align with Denison University's sustainability goals. Denison is embarking on a journey to add more  electric vehicle (EV) charging infrastructures on campus, a significant step towards encouraging the adoption of EVs among our community members. Therefore, our motivation is to drive Denison University towards a future where EVs play a central role in reducing our carbon footprint. With five chargers supporting the university's vehicle fleet transition to electric vehicles and facilitating personal electric vehicle usage for faculty, staff, and students, the project aims to explore potential opportunities and optimize charging strategies.
To be successful, we must have a clear understanding of EV user behavior and the flexibility to optimize infrastructure and policy. Our recommendations will be rooted in rigorous data insights, ensuring they reflect the real needs and potentialities of the University. Moreover, it is not just to provide EV charging but to transform Denison into a hub of sustainable mobility, making a positive impact on our community, environment, and the future of transportation. 
### Authors
We are a dedicated group of students at Denison University, each specializing in diverse academic fields. This collaborative project is a part of our coursework in the DA 301-01 Practicum in Data Analytics, supervised by Professor Alexandre Scarcioffolo.

Our team comprises four highly motivated members, each bringing unique skills and expertise to the table:
- **Chi Vu (Class of 2024)**
  - Majors: Global Commerce and Data Analytics
  - vu_c1@denison.edu
  
- **Ha-My Nguyen (Class of 2024)**
  - Major: Computer Science
  - nguyen_m3@denison.edu

- **Suryansh (Class of 2025)**
  - Major: Data Analytics and Financial Economics
  - agrawa_s1@denison.edu

- **Lena Le (Class of 2024)**
  - Majors: Psychology and Data Analytics
  - le_a2@denison.edu

Together, we form a dynamic team with a shared passion for data analysis and a commitment to making a positive impact on Denison University's sustainability efforts.
### BuildStatus
In certain instances in the dataset "charging_points_data", even when the "Charging Time" (hh:mm:ss) is non-zero, we encounter a situation where the associated value in the "Energy (kWh)" column remains zero. We have not found the answers of why this happens in our dataset, since if a vehicle's Charging Time is not zero, we would expect the Energy Consumption to also be non-zero. Additionally, we created a new variable named “Idle time” by subtracting values in “Total Duration (hh:mm:ss)” by “Charging Time (hh:mm:ss)” in our "Denison EVC v2" dataset. From this new variable, there is a new error such that some idle times turn out to be negative. However, "Total Duration" should always be bigger than "Charging Time", thus negative values are impossible. We have not found the answers for this error as well, so we decided to remove these negative values out of our statistical tests. 

### Requirements

### CodeFiles
### DataFiles
The EV chargers at Denison University are manufactured by Charge Point, which is named "charging_points_data". This is a CSV file of raw data directly from Charge Point system for usage on Denison campus for 5 charging stations in the parking lots of: Michael D. Eisner Center for the Performing Arts, Mitchell Recreation and Athletics Center, Swasey Chapel, Slayter Hall Student Union (P1), Granville Inn.

Secondly, we created a CSV file of clean data after processing from the "charging_points_data", which is called "Denison EVC v2". 
| Data file name     | Folder  | Description | Usage |
|----------|------|------------|----------|
| charging_points_data     | \Denison Data  | The EV chargers at Denison University are manufactured by Charge Point.This is a CSV file of raw data directly from Charge Point system on Denison campus for 5 charging stations in the parking lots of: Michael D. Eisner Center for the Performing Arts, Mitchell Recreation and Athletics Center, Swasey Chapel, Slayter Hall Student Union (P1), Granville Inn. | Pre-processing data for reference|
|  Denison EVC v2  | 28   | CSV file of clean data. We removed data points with zero or null values for variable “Energy (kWh)”, and created new variable “Idle time” by subtracting values in “Total Duration (hh:mm:ss)” by “Charging Time (hh:mm:ss)” | Post-processing data for analysis |
| Michael  | 35   | Writer  |jiji|

### Illustrations
### HowToUse
### Contribute
### Credits

