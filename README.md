# python-assignment-part4
# Student Performance Analysis & Prediction - Assignment Part 4

This is my project for predicting whether students will pass or fail based on their grades and habits. I used a small dataset of 15 students to walk through the entire data science process, from exploration to machine learning.

### Task 1: Data Exploration
I used Pandas to load the `students.csv` file and look at the basic statistics.
* I used `.head()` and `.describe()` to understand the distributions.
* I calculated the average scores for each subject, comparing students who passed vs. those who failed.
* I also identified the student with the highest overall average.

### Task 2 & 3: Visualizing the Trends
I created several plots to see how different factors like study hours and attendance affect grades.
 
* **Matplotlib Plots:** I made a bar chart for average scores, a histogram for math, a scatter plot for study hours, a box plot for attendance, and a line plot comparing math vs. science scores.
* **Seaborn Plots:** I used subplots to compare math and science scores by pass/fail status and created a scatter plot with a regression line to see the trend in attendance.
* **Comparison:** In my code comments, I've noted that I found Seaborn much faster for styling, while Matplotlib was better for building the custom line and box plots exactly how I wanted.
* **Colors:** For colors, I deliberately used specific hex codes (like `#2ecc71` for pass and `#e74c3c` for fail) throughout all plots to keep a consistent green = pass, red = fail theme across every chart.
 
### Task 4: Logistic Regression Model
* **Preprocessing:** I split the data (80/20) and used `StandardScaler` to make sure all features were on the same scale.
* **Evaluation:** I printed the training and test accuracy. Since the test set is small (only 3 students), I also printed a table showing the Actual vs. Predicted labels for each student to see where the model got it right (✅) or wrong (❌).
* **Feature Importance:** I extracted the model coefficients and made a horizontal bar chart. This shows which subjects (like Math or Science) have the biggest impact on passing.
* I also added `random_state=42` and `max_iter=200` to the model to make sure the results are reproducible every time the notebook runs.
 
  

### Files in this Repository:
* `part4_vizualization_ml.ipynb` — The main notebook with all my code and outputs.
* `students.csv` — The dataset used for the analysis.
* `plot1_bar.png` — Bar chart of average score per subject.
* `plot2_histogram.png` — Histogram of math score distribution.
* `plot3_scatter.png` — Scatter plot of study hours vs average score.
* `plot4_boxplot.png` — Box plot of attendance by pass/fail.
* `plot5_line.png` — Line plot of math and science scores per student.
* `plot6_seaborn_bar.png` — Seaborn bar chart comparing math and science by pass/fail.
* `plot7_seaborn_scatter.png` — Seaborn scatter plot with regression lines for attendance vs average score.
* `plot8_feature_importance.png` — Horizontal bar chart of logistic regression coefficients from Task 4.
