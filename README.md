# Electric-Vehicle-EV-Market-Analysis


Electric Vehicle (EV) Market Analysis Adoption trends, consumer preferences and fleet profile of Washington State Final project.


This project profiles the electric vehicle fleet recorded by the Washington State Department of Licensing. It asks which vehicle types, makes and models dominate, how the fleet has grown by model year, how electric range varies, and where the vehicles are concentrated. The aim is to turn raw records into clear evidence for clean-mobility and charging-infrastructure planning.

# EV Market Analysis, Washington State: 
1. Data Loading
The project uses the Washington State Department of Licensing Electric Vehicle Population Data from Data.gov: 299,705 raw records of battery electric (BEV) and plug-in hybrid (PHEV) vehicles. The CSV was uploaded in Google Colab and read into a pandas DataFrame, then previewed to confirm columns such as county, city, model year, make, model, vehicle type, CAFV eligibility and electric range.
2. Data Cleaning
Cleaning left 299,694 usable records and made the range data trustworthy. The steps were:
Standardised column names to lowercase and trimmed whitespace; blanks became true missing values.
Checked duplicates (0 exact rows, 0 repeated vehicle IDs).
Treated an electric range or price of 0 as "not recorded" and dropped 11 rows missing county, city or postal code.
Standardized text case, converted model year to integer, padded postal codes to 5 digits, and removed impossible values.
Flagged 1,299 electric-range outliers with the IQR rule (separately for BEV and PHEV), then replaced them with the median of the same make, model and year where possible.
3. Exploratory Data Analysis and Visualizations
EDA moved from single variables to comparisons, using labelled charts with counts on every bar:
Fleet composition: BEV vs PHEV, CAFV eligibility, top makes and models, range and model-year distributions.
Trends: records and median range by model year, cumulative growth, and top-5 makes over time.
Geography: top counties, cities, legislative districts and utilities, plus a county concentration curve.
Comparisons: BEV/PHEV mix and median range by manufacturer, CAFV by vehicle type, and the model year vs range correlation.
4. Project Document Report
Washington's EV fleet is overwhelmingly battery electric, dominated by Tesla, and concentrated in a few counties, but two-thirds of records lack range data, so range conclusions are limited. 
4.1 Objective and scope
The goal was to describe the Washington State EV fleet (types, makes, model years, electric range and location) and turn raw registration records into evidence for clean-mobility and charging-infrastructure planning. The analysis covers 299,694 cleaned records from the Department of Licensing.
4.2 Approach
Loaded and profiled the data in Google Colab with pandas, matplotlib and seaborn.
Cleaned it: standard names and text, duplicate check, impossible values removed, 1,299 range outliers treated.
Explored it with single-variable, trend, geographic and group-comparison charts, each labelled with counts and caveats.
Collected the findings from the charts.
