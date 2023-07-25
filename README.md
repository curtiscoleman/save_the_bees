# Save the Bees!!
![Honeybees](https://cdn.mos.cms.futurecdn.net/HixjyeXYJCrSDVGkZTmprP-1024-80.jpg.webp)

<font size="1"> In this project I will be comparing census data on honeybees to that of US citizens to determine a ratio! (Note: This project was just for fun. It does not use up-to-date data and should not be used for research purposes)
Data used for the comparison is from 2010-2012.
In order to run this project please do the following:

1. Clone the repository from GitHub using the link above. 
2. Activate the virtual environment as per you choice of command prompt/power shell.
3. Install the packages listed in the "requirements.txt" file.
4. Open the file in whichever editor suits you best.

Requirements satisfied:
1. Two separate CSV files loaded in.
2. CSV files converted into Pandas DataFrames and cleaned.
3. CSV files merged.
4. One Pandas pivot table.
5. Two visualizations.
6. One Tableau Workbook.
7. Code is annotated throughout.
8. Markdown language utilized.
9. Data dictionary included.

### Data Sources:
https://data.world/finley/bee-colony-statistical-data-from-1987-2017/workspace/file?filename=Bee+Colony+Census+Data+by+County.csv

https://www.kaggle.com/datasets/peretzcohen/2019-census-us-population-data-by-state

### Tableau Workbook: 
    https://public.tableau.com/authoring/HoneybeeProject/Sheet1#1

# Data Dictionary

## "bee_data" DataFrame:
Year (integer): The year of the census data.
State (string): The name of the state where the data was collected.
Value (float): The estimated population of honeybees in the state for the given year.
## "us_data" DataFrame:
NAME (string): The name of the state or territory in the United States.
POPESTIMATE2010 (integer): The estimated population of the state in the year 2010.
POPESTIMATE2011 (integer): The estimated population of the state in the year 2011.
POPESTIMATE2012 (integer): The estimated population of the state in the year 2012.
## "clean_bee_data" DataFrame:
STATE (string): The name of the state.
BEEPOP (float): The estimated population of honeybees in the state, calculated by multiplying the 'Value' by the 'avg_colony_pop' (average colony population) constant.
## "clean_us_data" DataFrame:
NAME (string): The name of the state or territory in the United States (uppercase).
USPOP (float): The estimated population of the state in the years 2010 to 2012, calculated by taking the mean of 'POPESTIMATE2010', 'POPESTIMATE2011', and 'POPESTIMATE2012'.
## "combined_data" DataFrame:
STATE (string): The name of the state.
BEEPOP (float): The estimated population of honeybees in the state, given in millions.
USPOP (float): The estimated population of the state in the years 2010 to 2012, given in millions.
## "pivot_table" DataFrame:
STATE (string): The name of the state.
BEEPOP (string): The estimated population of honeybees in the state, formatted as 'X.XM' (X million).
USPOP (string): The estimated population of the state in the years 2010 to 2012, formatted as 'X.XM' (X million).
## "totals_data" DataFrame:
'' (string): An empty string representing the total population data for the entire United States.
BEETOTAL (float): The total estimated population of honeybees in the United States, given in millions.
USTOTAL (float): The total estimated population of the United States in the years 2010 to 2012, given in millions.