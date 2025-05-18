COVID-19 Global Data Tracker

Overview
The COVID-19 Global Data Tracker is a Jupyter Notebook project that analyzes global COVID-19 data from the Our World in Data COVID-19 dataset. It performs data cleaning, exploratory data analysis (EDA), visualizations, and statistical computations to provide insights into cases, deaths, and vaccination rates worldwide.
Features

Data Cleaning: Handles missing values and formats dates.
Visualizations:
Time-series plots for total cases, deaths, and new cases (7-day moving average) for selected countries (e.g., Kenya, USA, India).
Interactive choropleth map of global total cases.


Statistics:
Top 5 countries by total cases, deaths, and vaccination rates.
Global totals for cases, deaths, and vaccinations.
Global average death rate (deaths/cases).


Outputs:
PNG plots: total_cases_time_series.png, total_deaths_time_series.png, new_cases_smoothed.png.
HTML map: covid_global_map.html.
Tables and stats printed in the notebook.



Prerequisites

Python 3.8+
Jupyter Notebook or Jupyter Lab
Dependencies:pip install pandas matplotlib seaborn plotly


Jupyter Lab (optional for Plotly):jupyter labextension install jupyterlab-plotly


Dataset:
Download owid-covid-data-old.csv from Our World in Data.
Place it in the project root.



Setup

Clone the Repository:
git clone https://github.com/zippyrehema123/covid-global-data-tracker-project.git
cd covid-19-global-data-tracker


Install Dependencies:
pip install -r requirements.txt

Or manually:
pip install pandas matplotlib seaborn plotly


Download the Dataset:

Save owid-covid-data.csv in the project root.
Update the notebook’s file path if stored elsewhere.


Launch Jupyter Notebook:
jupyter notebook

Open covid_data_tracker.ipynb.


Usage

Run the Notebook:

Open covid_data_tracker.ipynb in Jupyter Notebook.
Execute cells in order (Shift + Enter) to:
Load and clean data (owid-covid-data.csv).
Generate time-series plots for selected countries.
Create a global choropleth map.
Compute statistics (top countries, global totals, death rate).




View Outputs:

Plots: Display inline and saved as PNGs in the project directory.
Map: Displays inline and saved as covid_global_map.html (open in a browser).
Statistics: Printed tables and metrics in the notebook.


Customize:

Edit countries_of_interest in the notebook (e.g., ['Brazil', 'Germany']) to analyze other countries.
Modify plot styles (e.g., colors, scales) or add metrics (e.g., case fatality rates).



File Structure
covid-19-global-data-tracker/
├── covid_data_tracker.ipynb      # Jupyter Notebook
├── owid-covid-data.csv           # Dataset (download separately)
├── total_cases_time_series.png   # Output: Cases plot
├── total_deaths_time_series.png  # Output: Deaths plot
├── new_cases_smoothed.png        # Output: New cases plot
├── covid_global_map.html         # Output: Choropleth map
├── README.md                     # Project documentation


Example Outputs

Time-Series Plot:
Choropleth Map:Open covid_global_map.html in a browser for an interactive view.
Statistics (example):Top 5 countries by total cases:
        location  total_cases
0  United States  100000000.0
1         India   45000000.0
...

Global average death rate: 1.00%



Troubleshooting

FileNotFoundError: owid-covid-data.csv:
Ensure the dataset is in the root directory or update the path in the notebook.


ModuleNotFoundError:
Install dependencies: pip install pandas matplotlib seaborn plotly.


Choropleth Map Not Displaying:
Install Plotly extension for Jupyter Lab: jupyter labextension install jupyterlab-plotly.
Ensure internet access for map tiles.


Empty Plots/Tables:
Check country names: print(df['location'].unique()).
Verify data: print(df[['total_cases', 'total_deaths']].isnull().sum()).



Contributing

Fork the repository.
Create a branch: git checkout -b feature-name.
Commit changes: git commit -m "Add feature".
Push: git push origin feature-name.
Open a pull request.


Acknowledgments
Data: Our World in Data
Libraries: pandas, matplotlib, seaborn, Plotly

