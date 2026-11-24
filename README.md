# Experiment 2: Data Visualization Using Matplotlib and Seaborn

## Aim

To visualize data using Matplotlib and Seaborn libraries.

## Algorithm

1.  **Start.**
2.  Import the Matplotlib and Seaborn libraries.
3.  Load data into a Pandas DataFrame.
4.  Plot a histogram for age distribution using `plt.hist()`.
5.  Plot a scatter plot for Age vs. Salary using `sns.scatterplot()`.
6.  Plot salary distribution using `sns.boxplot()`.
7.  Show the plots sequentially.
8.  **Stop.**

## Program

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Step 3: Load data into a Pandas DataFrame
data = {
    "Age":    [22, 25, 27, 29, 31, 33, 35, 38, 41, 45, 48, 52],
    "Salary": [28000, 32000, 36000, 41000, 47000, 52000,
               58000, 64000, 71000, 79000, 86000, 120000]
}
df = pd.DataFrame(data)
print(df.head())

# Step 4: Histogram of Age
plt.figure(figsize=(6, 4))
plt.hist(df["Age"], bins=6, color="skyblue", edgecolor="black")
plt.title("Age Distribution")
plt.xlabel("Age")
plt.ylabel("Frequency")
plt.savefig("images/histogram.png")
plt.show()

# Step 5: Scatter plot of Age vs Salary
plt.figure(figsize=(6, 4))
sns.scatterplot(x="Age", y="Salary", data=df, color="green")
plt.title("Age vs Salary")
plt.savefig("images/scatter.png")
plt.show()

# Step 6: Box plot of Salary
plt.figure(figsize=(6, 4))
sns.boxplot(y=df["Salary"], color="orange")
plt.title("Salary Distribution")
plt.savefig("images/boxplot.png")
plt.show()
```

## Output

**Dataset (first 5 rows):**

```
   Age  Salary
0   22   28000
1   25   32000
2   27   36000
3   29   41000
4   31   47000
```

**1. Histogram: Age Distribution**

<img width="645" height="481" alt="image" src="https://github.com/user-attachments/assets/c5c6fa31-4c80-4e1a-81fb-dee8da052a6f" />


**2. Scatter Plot: Age vs Salary**

<img width="680" height="481" alt="image" src="https://github.com/user-attachments/assets/0cdddae2-8209-4bfb-99cd-f515e0691e1f" />


**3. Box Plot: Salary Distribution**

<img width="680" height="428" alt="image" src="https://github.com/user-attachments/assets/64bf5a41-6030-43b8-992d-c0f7fdba1757" />


## Result

The program was executed successfully, and the data was visualized using
Matplotlib and Seaborn.

-   The **histogram** shows how employee ages are distributed across
    different age groups.
-   The **scatter plot** shows a positive relationship between Age and
    Salary: salary increases as age increases.
-   The **box plot** shows the median, quartiles and spread of salary, and
    highlights the highest salary as a possible outlier.

Thus, Matplotlib and Seaborn were used to visualize data effectively.
