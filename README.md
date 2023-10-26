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
    <li><a href="#Acknowledgement">Acknowledgement</a></li>
  </ol>
</details>

## Motivation
Our primary motivation is to align with Denison University's sustainability goals. Denison is embarking on a journey to add more  electric vehicle (EV) charging infrastructures on campus, a significant step towards encouraging the adoption of EVs among our community members. Therefore, our motivation is to drive Denison University towards a future where EVs play a central role in reducing our carbon footprint. With five chargers supporting the university's vehicle fleet transition to electric vehicles and facilitating personal electric vehicle usage for faculty, staff, and students, the project aims to explore potential opportunities and optimize charging strategies.
To be successful, we must have a clear understanding of EV user behavior and the flexibility to optimize infrastructure and policy. Our recommendations will be rooted in rigorous data insights, ensuring they reflect the real needs and potentialities of the University. Moreover, it is not just to provide EV charging but to transform Denison into a hub of sustainable mobility, making a positive impact on our community, environment, and the future of transportation. 

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Authors
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

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## BuildStatus
In certain instances in the dataset "charging_points_data", even when the "Charging Time" (hh:mm:ss) is non-zero, we encounter a situation where the associated value in the "Energy (kWh)" column remains zero. We have not found the answers of why this happens in our dataset, since if a vehicle's Charging Time is not zero, we would expect the Energy Consumption to also be non-zero. Additionally, we created a new variable named “Idle time” by subtracting values in “Total Duration (hh:mm:ss)” by “Charging Time (hh:mm:ss)” in our "Denison EVC v2" dataset. From this new variable, there is a new error such that some idle times turn out to be negative. However, "Total Duration" should always be bigger than "Charging Time", thus negative values are impossible. We have not found the answers for this error as well, so we decided to remove these negative values out of our statistical tests. 

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Requirements
To run the code and analysis for this project, we will need the following software and packages:

- **RStudio** (Version 2023.09.1+494) - For data analysis and statistical modeling.
- **Packages:**
  - `tidyverse` - Used for data manipulation and visualization.
  - `readr` - Used for reading and handling data.
  - `Anova` - Required for conducting statistical Anova tests.
  - `post hoc` - For post-hoc analyses.
- **Excel** -  **Excel for Mac (version 16.67), running on macOS Big Sur 11.5.2** for data cleaning in preparation for statistical tests.
- **Tableau** - Require **Tableau Desktop Professional Edition (Version 2023.2.0)** or later for data visualization.

Please ensure you have the specified software and packages installed and configured to effectively run the code, access the data, and view the analysis output.


<p align="right">(<a href="#readme-top">back to top</a>)</p>

## CodeFiles
Include R file from Lena 

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## DataFiles
All included under folder named “DATA” on shared Drive
| Data file name     | Access  | Description | Usage |
|----------|------|------------|----------|
| charging_points_data     | Can be accessible through Charge Point account with consent of Denison Sustainability Department | The EV chargers at Denison University are manufactured by Charge Point.This is a CSV file of raw data directly from Charge Point system on Denison campus for 5 charging stations in the parking lots of: Michael D. Eisner Center for the Performing Arts, Mitchell Recreation and Athletics Center, Swasey Chapel, Slayter Hall Student Union (P1), Granville Inn. | Pre-processing data for reference|
|  Denison EVC v2  | Private   | CSV file of clean data. We removed data points with zero or null values for variable “Energy (kWh)”, and created new variable “Idle time” by subtracting values in “Total Duration (hh:mm:ss)” by “Charging Time (hh:mm:ss)”. | Post-processing data for analysis |
| Utility Data for DA students.xlsx  | Private   | CSV data file from Denison Sustainability department detailing overall energy use and cost across campus.  |Reference for correlation between energy consumption with EV charging facility on Denison campus|
| Station_Provision_Logs-20231009Kenyon  | Private  | Raw CSV data file directly from Charge Point system for usage on Kenyon College campus  | Reference for usage comparision and analysis|

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Illustrations
Include one output from Lena's works

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## HowToUse
To access and utilize the data and findings from this project, please follow these steps:
1. **Create a Charge Point Account:** Begin by creating an account on Charge Point using the following link: [Charge Point Account Creation](https://www.chargepoint.com/drivers/activate).
2. **Request Access to Denison Charging Points Data:** Since our data is private, you can request access to the "charging_points_data" from Denison Sustainability Department. For more information and access requests, please visit the Denison Sustainability Department website: [Denison Sustainability Department](https://denison.edu/campus/green).

These steps will allow you to access our analysis and findings for this project, as well as the relevant data. If you have any further questions or need assistance, please feel free to contact us.
  
<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Contribute
Contributions are what make the open source community such an amazing place to learn, inspire, and create. While we appreciate your interest in contributing, please note that this project is closely aligned with the Denison University Sustainability Department and our DA 301-01 class. 

Here's how you can get involved:

- **Analyze Data:** Feel free to conduct your own analysis. You can find the data on Charge Point by creating your own account and accessing the relevant pre-processing resources.

- **Provide Feedback:** If you have suggestions to improve the project or any insightful observations, please share your thoughts. You can do this by opening an issue with the tag "enhancement."

However, please be aware that any external analyses and contributions will not be merged into our code files or change our project documents. This distinction helps maintain the integrity of the project while allowing you to explore and build upon the data.

Our practice respects our clients' discretion in sharing our analysis and findings with the public. If you have any additional inquiries, please don't hesitate to reach out to us via our email address or through the Denison Sustainability Department.   

We appreciate your support and thank you for your understanding

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Acknowledgement
We would like to express our gratitude to the following individuals and organizations for their invaluable contributions and support throughout this project:

**Consultants:**
- **Chris Wolfington**
  - *Principal Consultant, Ground Truth Energy*
- **Hannah Ruscin**
  - *Program Manager, Drive Electric Ohio*
    
These dedicated consultants provided us with crucial background knowledge and deep insights into the topics we explored.

**Denison University:**
- **John Bishop**
  - *Director of Business Services, Denison University*
- **Jeremy King**
  - *Director of Sustainability & Campus Improvement, Denison University*
    
We appreciate Denison's Sustainability Department for entrusting us with this project and for their valuable feedback that has significantly enhanced the quality of our work.

**Professor Alexandre Scarcioffolo:**
- **Denison University**
  
We extend our gratitude to Professor Alexandre Scarcioffolo for his unwavering support, guidance, and feedback throughout the project. His mentorship has been instrumental in our journey.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
