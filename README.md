# EnergyPlus Dashboard

Data scrapers were created in a Jupyter Notebook. There is a notebook for each city. The process includes:

* Documents necessary energy conversions (summary CSV does this...but not using the summary using the output CSV that has all the reporting data).
* Holds variable for gas and elec pricing.
* Combines all EnergyPlus default CSV files in defined directory.
* Grabs the wanted columns from the merged dataframe. Renamed columns. Cleaned data if necessary.
* Gets the annual energy data
    * Uses the pricing variable to convert to costs.
    * Combines the annual data and costs into grouped dataframe.
    * Exports annual data to CSV.
* Gets the monthly energy data
    * Uses the pricing variable to convert to costs.
    * Combines the monthly data and costs into grouped dataframe.
    * Exports monthly data in CSV.
    * Finds the average illuminance for each month.
    * Exports illuminance data to CSV.
* Gets the hourly energy data
    * Uses the pricing variable to convert to costs.
    * Combines the monthly data and costs into dataframe.
    * Exports hourly data to CSV.
* Creates conditionals
    * Exports hourly data will illumnation greater than 200 lux.
    * Exports hourly conditional data to CSV.
    * Performance targets will be determined in Tableau from this reduced dataset.

* All CSVs brought into Tableau for graphing/charting.

