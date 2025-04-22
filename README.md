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





