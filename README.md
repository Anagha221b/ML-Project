# Energy Consumption Analysis using Predictive Analytics


Columns and their description:

customer_id: Unique identifier for each customer.

region: Geographic region of the customer.

energy_consumption_kwh: Total energy consumption in kilowatt-hours.

peak_hours_usage: Energy usage during peak hours.

off_peak_usage: Energy usage during off-peak hours.

renewable_energy_pct: Percentage of energy from renewable sources.

billing_amount: Total billing amount.

household_size: Number of people in the household.

temperature_avg: Average temperature.

income_bracket: Income bracket of the household.

smart_meter_installed: Whether a smart meter is installed.

time_of_day_pricing: Whether time-of-day pricing is used.

annual_energy_trend: Annual trend in energy consumption.

solar_panel: Whether solar panels are installed.

target_high_usage: Whether the household is targeted for high usage.

Operations performed on the dataset:

1.	Data Loading (pd.read_csv()):

The code starts by loading the energy dataset from a CSV file into a pandas DataFrame. This is the standard way to ingest tabular data in Python for data analysis and machine learning.

2.	Outlier Removal (remove_outliers() function):

A custom function remove_outliers is defined to identify and remove outliers from specified numerical columns using the Interquartile Range (IQR) method.

For each specified column:

The first quartile (Q1) and third quartile (Q3) are calculated.

The IQR (Q3 - Q1) is computed.

Lower and upper bounds are determined as Q1 - 1.5 * IQR and Q3 + 1.5 * IQR, respectively.

Data points outside these bounds are filtered out, effectively removing the outliers.

3.	Exploratory Data Analysis (EDA) and Visualization (matplotlib.pyplot, seaborn):

The code includes several steps for visualizing the data to understand its characteristics:

df.hist(): Generates histograms for all numerical features to visualize their distributions.

sns.boxplot(): Creates box plots for numerical features to visually identify outliers and understand the spread of the data.

sns.pairplot(): Displays pairwise relationships between numerical features, helping to identify potential correlations and patterns.

sns.heatmap(): Generates a heatmap of the correlation matrix between numerical features, quantifying the linear relationships between them.

df.groupby(...).plot(kind='bar'): Creates bar plots to visualize aggregated data based on categorical features like 'region' and 'income_bracket'. This helps in understanding the relationship between these categories and energy consumption or billing amount.

df['household_size'].value_counts().plot(kind='bar'): Shows the distribution of household sizes.

These visualizations provide insights into the data's distribution, potential outliers (though outliers are removed before this), and relationships between variables. 








