Python Code to Generate the Graph

This updated script uses the new dataset and includes the linear regression projection. 
It plots historical data as a solid line and projections as a dashed line for clarity. Requires pandas, matplotlib, and 
scikit-learn (install with pip install scikit-learn if needed). Run it in a Python environment to visualize.

Explanation of the Code and Projection

Data Loading: Hardcoded list converted to a pandas DataFrame.
Linear Regression: Uses scikit-learn to fit a line to historical points (time in approximate months vs. occupation %). Slope 
(~0.11% per month) reflects the post-2022 creep.
Plotting: Solid red line for history, dashed lighter red for projections. Annotations highlight events that deviated from the trend.
Projection Logic: Extrapolates from September 2025 onward, adding ~2.75% over 2 years (to ~25.3% by Sep 2027). To arrive at this: 
(1) Compute months elapsed from baseline; (2) Fit y=mx+by = mx + by = mx + b
 via least squares; (3) Predict for future months t+24t + 24t + 24, where ( t ) is the last historical month.
Output: Displays the plot; add plt.savefig('russia_occupation_projection.png') to export.

