
# Mobile Analysis Project

## Overview
This project analyzes mobile phone data to provide insights on various attributes such as brand performance, pricing trends, and specifications. The analysis leverages MySQL to manage and query the data effectively.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup](#setup)
- [Data Structure](#data-structure)
- [Data Analysis](#data-analysis)
- [Results](#results)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Features
- Comparative analysis of mobile phone brands and models
- Insights into pricing trends and storage capacities
- Analysis of features such as camera quality and battery capacity
- Visualization of key metrics (if applicable)

## Technologies Used
- **Database:** MySQL
- **Programming Language:** SQL
- **Data Visualization Tools:** (e.g., Python with Matplotlib, Tableau)

## Setup
1. **Clone the Repository**
   ```bash
   git clone https://github.com/Sachindanaji/mobile-analysis.git
   cd mobile-analysis


## Import Database
- Create a database
CREATE DATABASE mobile_analysis;

- Import the dataset (if you have a SQL dump):
mysql -u root -p mobile_analysis < data_dump.sql

## Data Structure
The dataset contains the following columns:

- Phone_name: Name of the mobile phone
- Brands: Manufacturer of the phone
- Price: Price of the phone (in currency)
- Internal_Storage: Internal storage capacity (in GB)
- Operating_System_Type: Type of operating system (e.g., Android, iOS)
- USB_Type: Type of USB port (e.g., USB-C, Micro-USB)
- 5G_Availability: Indicates if the phone supports 5G (Yes/No)
- Selfie_Camera: Resolution of the selfie camera (in MP)
- RAM_Storage: RAM capacity (in GB)
- Country_of_Origin: Country where the phone is manufactured
- Battery_Capacity: Battery capacity (in mAh)
- Price_Range: Categorization of the price (e.g., Budget, Mid-range, Premium)
- Battery_Capacity_Range: Categorization of battery capacity (e.g., Low, Medium, High)
- Total_Mobile: Total count of mobile phones in the dataset

## Data Analysis
## Sample Queries
Here are some example SQL queries used for analysis:

1.Average Price by Brand:

SELECT Brands, AVG(Price) AS Average_Price
FROM mobile_data
GROUP BY Brands
ORDER BY Average_Price DESC;

2.Count of Phones Supporting 5G:

SELECT COUNT(*) AS Total_5G_Phones
FROM mobile_data
WHERE 5G_Availability = 'Yes';

3.Distribution of Battery Capacities:

SELECT Battery_Capacity_Range, COUNT(*) AS Count
FROM mobile_data
GROUP BY Battery_Capacity_Range;

## Results
- Brand Performance: Summarize findings related to which brands offer the best value or highest specs.
- Price Insights: Highlight trends in pricing relative to features like RAM and storage.
- Battery Capacity Trends: Discuss any patterns observed in battery performance across different price ranges.

## Usage
1.Connect to the Database Use a MySQL client or command line:
mysql -u root -p mobile_analysis

2.Execute Queries Run the provided SQL queries to explore the data and derive insights.

## Contributing
Contributions are welcome! Please read the CONTRIBUTING.md for guidelines.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
### Additional Suggestions:
- **Results Section:** Include specific findings or insights that emerged from your analysis.
- **Visuals:** If you created any graphs or charts, consider adding them to illustrate your findings.
- **Real-World Applications:** Discuss how your analysis could impact mobile marketing strategies or development choices.

Feel free to modify any sections to better reflect your work and findings! If you have any specific aspects you want to highlight or need help with, just let me know!
