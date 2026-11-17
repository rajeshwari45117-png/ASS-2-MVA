# ASS-2-MVA

Kendall, Pearson and Spearman Correlation Analysis
Overview
This notebook compares three correlation measures---Kendall's Tau,
Pearson's correlation, and Spearman's rank correlation---using simulated
data. It also examines the correlations produced by independent random
variables under the null hypothesis (H0).
Objectives
- Generate synthetic documentary-rating and education-level data.
- Calculate Kendall, Pearson, and Spearman correlation coefficients.
- Compare the three measures on the same data.
- Simulate repeated independent samples under H0 and examine squared
  correlation errors.
- Visualize the simulation results and the relationships among the
  correlation estimates.
Tools and Libraries
- Python
- NumPy
- SciPy (scipy.stats)
- Matplotlib
Notebook Workflow
1. Generate sample data
The notebook creates 40 observations: - docuRatings: random integer
documentary ratings from 1 to 5. - eduLevel: an education-level
variable generated from documentary ratings plus random variation,
scaled into levels 1 to 4.
2. Calculate correlations
The notebook calculates: - Kendall's Tau using
scipy.stats.kendalltau - Pearson correlation using
scipy.stats.pearsonr - Spearman rank correlation using
scipy.stats.spearmanr

The coefficients are rounded to four decimal places and displayed with a
scatter plot of education level against documentary ratings.
3. Simulation under H0
To study correlation estimates when there is no designed relationship,
the notebook runs 1,000 experiments. Each experiment generates two
independent random variables with 50 observations and 6 possible
categories, then calculates all three correlation coefficients.
4. Visualizations
The notebook produces: - A bar chart with error bars for the mean
squared correlation values. - A line plot showing the first 100
experiments' correlation estimates. - A heatmap of the correlation
matrix among the three sets of estimates.
Key Concepts
  Measure         What it measures
  Kendall's Tau   Association based on concordant and discordant pairs
Pearson         Linear relationship between numerical variables
Spearman        Monotonic association based on ranks
How to Run
1. Clone or download this repository.
2. Install the required libraries:
   pip install numpy scipy matplotlib jupyter
3. Start Jupyter Notebook:
   jupyter notebook
4. Open 28_stats_corr_Kendall (1).ipynb and run the cells in order.
Notes
The data is simulated in the notebook; it is not a real-world survey or
movie-rating dataset. Randomly generated values can vary between runs
because no random seed is set in this notebook.
Author
Add your name here.
