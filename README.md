## To The United Kingdom!

# Project Overview
This project ranks countries based on their readiness to face climate change and their overall livability, focusing on factors such as climate resilience, government stability, economic capacity, access to higher education, and cost of living. The United Kingdom (UK) emerged as the top contender through data analysis, which integrated various components from the ND-GAIN Index, specifically: readiness, economic capacity, government capacity, health risks, fresh water availability, higher education rankings, and cost of living. The goal was to identify the best country for relocation, with the UK as an ideal choice.

## Objective
The objective of this project is to provide a comprehensive ranking of countries by integrating various climate resilience and livability factors into a single composite score. By focusing on the country’s readiness for climate change and minimizing its vulnerabilities, we determined the most suitable countries for relocation. This analysis uses data from multiple sources, providing a holistic view of climate adaptability, health risk mitigation, access to resources, and educational opportunities.

## Tools Used
- **R**: The main programming language used for data manipulation, analysis, and visualization.

### Libraries:
- **readr**: for reading data from CSV files.
- **dplyr**: for data manipulation and transformations.
- **tidyr**: for reshaping and cleaning data.
- **scales**: to scale data for better comparison across different variables.

## Skills Applied
- **Data Importing and Cleaning**: I used `read_csv()` and `merge()` to import multiple datasets and merge them based on country abbreviations. I then cleaned the data to focus only on relevant columns and removed rows with missing data.
- **Data Transformation and Scaling**: I used `mutate()` and `rescale()` to standardize numerical columns, ensuring that all factors could be compared on the same scale.
- **Algorithm Development**: I created two main scores—Readiness Rank and Vulnerability Rank—based on the factors that most impact the suitability of a country. These scores were combined into a Composite Score to rank the countries effectively.
- **Visualization**: I included visual aids (e.g., images) to make the analysis more engaging and accessible.

## Conclusion
The analysis revealed that the United Kingdom leads the pack in terms of climate change preparedness, education, and affordability. By focusing on factors such as government stability, economic capacity, access to education, and the overall cost of living, the UK offers an optimal combination of readiness and resilience. This approach to analyzing countries can be useful for people looking to relocate to a country that offers a balance of climate resilience, economic opportunities, and quality of life. The final composite score allowed me to rank countries and showcase the UK as the top choice for individuals looking for a stable and sustainable environment for the future.
