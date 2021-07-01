# EnergyPlus Dashboard

Data scrapers were created in a Jupyter Notebook. There is a notebook for each city. The process includes:

* Documents necessary energy conversions (summary csv does this...but not using the summary using the csv that has all the data).
* Holds variable for gas and elec pricing.
* Combines all EnergyPlus default csv files (not the summary) in defined directory.
* Grabs the wanted columns from the merged dataframe.
* Exports scenario names for filter.
* Gets the annual energy data
    * Uses the pricing variable to convert to costs.
    * Combines the annual data and costs into grouped dataframe.
    * Exports annual data in csv and json.
* Gets the monthly energy data
    * Uses the pricing variable to convert to costs.
    * Combines the monthly data and costs into grouped dataframe.
    * Exports monthly data in csv and json.
    * Finds the average illumance for each month.
    * Exports illuminance data in csv and json.


Preview at: <a href="https://klharp.github.io/EPlus-Dashboard-ODL/">klharp.github.io/EPlus-Dashboard-ODL</a>
