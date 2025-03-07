# Super Smash Bros. Data Analysis: Character Stats and Visualizations

## Introduction
In this project, I analyzed various Super Smash Bros. character statistics to uncover insights about character strengths, attributes, and performance. The dataset consisted of various attributes for each character, and I aimed to visualize this data to make comparisons more insightful.

Using **Pandas**, **Matplotlib**, and **Pandas Styler**, I cleaned and processed the data to generate visualizations that highlight key statistics for the characters. The project involved various challenges, including working with incomplete or messy data and exploring new ways to visualize data to make it more intuitive for users.

## Project Objectives
- **Data Cleaning and Preprocessing**
  - Load and clean the dataset, handling missing or inconsistent data.
  - Utilize **Pandas** for efficient data manipulation and analysis.

- **Statistical Analysis and Visualization**
  - Analyze character statistics to identify trends.
  - Implement visualizations with **Matplotlib** and **Pandas Styler** to display character attributes clearly.

- **Interactive Visualizations**
  - Create interactive plots and widgets to allow users to explore character stats dynamically.
  - Design user-friendly layouts for easier comparisons of character performance.

## Methodology

### Data Cleaning and Preprocessing
- Loaded the dataset into a **Pandas** DataFrame and explored its structure.
- Cleaned the data manually, but realized that I could have used **Pandas**' built-in functions to clean the data more efficiently (this will be part of future improvements).
- Segmented the dataset into different character categories based on their attributes and stats.

### Data Analysis
- Examined key character statistics, including attack power, speed, and defense.
- Aggregated the data to get a clear picture of overall character strength across the different attributes.

### Visualizations
- Used **Pandas Styler** to apply custom styles to DataFrames and present the data in a visually appealing way.
- Created horizontal bar charts with interactive scrollers to visualize the range of character stats.
- Struggled with some advanced visualization techniques but managed to implement basic visualizations that were useful for interpreting the data.

## Project Conclusion
In sum, this project was a success for what it was. I believe I exemplified my understanding of data analysis, manipulation, and visualization. Although this project was less math-heavy than the **CPI Inflation Modeling** project, it still presented challenges, especially in dealing with uncertainty. **Pandas** felt straightforward, but applying it in practical situations required some out-of-the-box thinking, especially with visualizations.

### Key Learnings and Improvements
- **Data Cleaning**: I should have used **Pandas** from the start to clean the data, instead of manually cleaning it. This would have saved a lot of time and effort.
- **Interactivity**: The scroller widget for controlling the range of bar chart values was not as effective as anticipated. I would simplify it in future projects by using a basic horizontal scroller.
- **Visual Enhancements**: I could have added a color gradient for the character dropdown and stats to make it more visually engaging. This would help users better understand the relative strength of characters at a glance.
- **Legend and Explanation**: I should have included a legend to explain what the colors represent in the visualizations, making the charts more intuitive for users.
- **User Experience**: If I had more time, I would have improved the overall user interface to make it more user-friendly and accessible, as suggested in my code review.

Despite these areas for improvement, this project was insightful and unique. Moving forward, I plan to dive deeper into how **Pandas** functions work and explore new data visualization techniques to enhance future projects.

## Research Conclusion: Pandas Styler and Visualization Techniques
**Pandas Styler** proved to be a great tool for visualizing data in a vibrant and engaging way. I also learned that **color gradients** can serve as effective indicators in data visualizations, helping users quickly assess the relative size or value of numbers.

During my research, I came across several interesting ways to improve visualizations. For instance, **Pandas Styler** allows you to substitute elements in an index column with images, which could be useful for displaying character icons instead of just names. Although I attempted to implement this feature, I faced some issues, but I plan to revisit this in the future.

In addition, I could have used emojis to represent the strength or weakness of characters in various categories, making the data more visually intuitive and fun. This idea can be a playful yet effective way to show rankings.

Overall, this was a fun exploration of **Pandas Styler**, and I’m excited to try these new visualizations in future projects. I plan to go back to my **Super Smash Bros.** analysis and apply some of these new ideas to further refine the project.

## Technologies & Tools Used
- **Pandas**: To manipulate and analyze data
- **Matplotlib**: To visualize data
- **Pandas Styler**: To apply custom styling and vibrant visualizations to DataFrames
- **Ipywidgets**: To create interactive elements like dropdowns and scrollers for exploring character stats
