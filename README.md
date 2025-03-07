# CPI Inflation Modeling: Analyzing Inflation Trends with Exponential and Alternative Models

## Introduction
This project explores inflation trends for essential commodities (meat, fuel, and grain) and luxury items (metals and plant extracts) from 1900 to 1920. By leveraging data science techniques, I aimed to analyze how inflation rates differ between these categories and determine the most effective modeling approach for capturing these trends.

Using **NumPy**, **Pandas**, **Matplotlib**, and **SciPy**, I implemented an exponential curve-fitting model to represent the growth of inflation rates. Additionally, I conducted further research to explore alternative modeling techniques—polynomial and logarithmic regression—to improve the accuracy of predictions, particularly for data sets where exponential models were insufficient.

## Project Objectives
- **Model Inflation Rates**
  - Load and preprocess CPI data for various products from 1900 to 1920.
  - Categorize products into essential commodities and luxury items.
  
- **Fit Exponential Curves**
  - Apply exponential regression to model inflation trends over time.
  - Assess the quality of fit for each product category.
  
- **Compare Growth Rates**
  - Analyze inflation trends among essential commodities and luxury items.
  - Identify key factors influencing inflation behavior.

## Methodology

### Step 1: Data Preparation & Initial Analysis
- Imported **NumPy** for numerical computations and **Pandas** for data manipulation.
- Visualized inflation trends using **Matplotlib** to identify patterns.
- Segmented products into essential commodities (meat, fuel, grain) and luxury items (metals, plant extracts).

### Step 2: Exponential Curve Fitting
- Used **SciPy**'s `curve_fit` function to apply exponential models to inflation rates.
- Evaluated model effectiveness by comparing growth trends among products.
- Found that essential commodities followed a consistent exponential trend, while luxury items showed irregular, volatile patterns that could not be effectively modeled using exponential functions.

### Step 3: Growth Rate Analysis
- Determined that **meat** had the highest inflation growth rate among essential commodities.
- Explored the potential impact of market vs. industry influence on inflation trends.
  - Essential commodities were largely market-driven, with inflation trends influenced by global demand.
  - Luxury items exhibited inconsistent trends, suggesting industry-specific rather than market-wide price fluctuations.

## Research Extension: Alternative Modeling Techniques
Given the limitations of exponential models for luxury items, I extended my research to explore alternative regression techniques:

- **Polynomial Regression**
  - A flexible approach that fits curved trends more accurately than exponential models.
  - Useful for datasets with nonlinear but structured variations.
  
- **Logarithmic Regression**
  - Best suited for rapid initial growth that levels off over time.
  - Helps model inflation trends that stabilize after an early increase.

### Findings from Alternative Models
- Polynomial regression provided a better fit than exponential models for the CPI data of essential goods.
- Logarithmic regression was useful for capturing trends with early rapid inflation, though its effectiveness varied.
- Overall, polynomial regression outperformed exponential regression, especially for essential commodities.

## Conclusion & Future Applications
Through this project, I successfully modeled and analyzed inflation trends using exponential regression and alternative modeling techniques. My key findings include:

- Essential commodities follow a clear exponential inflation trend, whereas luxury items exhibit more volatile behavior.
- Meat had the highest inflation growth rate, likely due to its widespread daily consumption.
- Market forces influence essential goods more predictably than luxury items, which are subject to industry-specific trends.
- Polynomial regression offers a better fit for essential commodities than exponential models.

This project not only strengthened my understanding of data science in financial modeling but also challenged me to explore alternative mathematical approaches to improve prediction accuracy. Moving forward, I plan to:
- Apply additional modeling techniques to broader financial datasets.
- Explore real-world applications of inflation modeling in finance and FinTech industries.
- Expand my knowledge of regression models to analyze more complex economic trends.

This project represents my first deep dive into data science applications in finance, and I look forward to refining these methods in future work.

## Technologies & Tools Used
- **NumPy** – Numerical computations
- **Pandas** – Data manipulation
- **Matplotlib** – Data visualization
- **SciPy** – Exponential curve fitting
- **Polynomial & Logarithmic Regression** – Alternative modeling techniques
  
## References
Abhigyan. (2020, August 2). Understanding Polynomial Regression!!! Medium. https://medium.com/analytics-vidhya/understanding-polynomial-regression-5ac25b970e18

Python Machine Learning Polynomial Regression. (n.d.). Www.w3schools.com. https://www.w3schools.com/python/python_ml_polynomial_regression.asp

Zach. (2020, September 9). Explanatory & Response Variables: Definition & Examples. Statology. https://www.statology.org/explanatory-response-variables/

Zach. (2021, March 30). Logarithmic Regression in Python (Step-by-Step). Statology. https://www.statology.org/logarithmic-regression-python/
