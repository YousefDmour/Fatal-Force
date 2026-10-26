# Fatal Force: Police Killings in the United States

This project explores fatal police shootings in the United States using data collected by [The Washington Post](https://www.washingtonpost.com/). The analysis combines police-shooting records with U.S. Census demographic and socioeconomic data to identify patterns by race, gender, age, location, state, poverty, and education.

## Project contents

```text
Fatal Force/
├── data/
│   ├── Deaths_by_Police_US.csv
│   ├── Median_Household_Income_2015.csv
│   ├── Pct_Over_25_Completed_High_School.csv
│   ├── Pct_People_Below_Poverty_Level.csv
│   └── Share_of_Race_By_City.csv
├── notebook/
│   └── Fatal_Force_(start).ipynb
├── requirements.txt
└── README.md
```

## Analysis included

The notebook covers:

- Initial dataset inspection, including shape, columns, missing values, and duplicates
- Average poverty and high-school graduation rates by state
- The relationship between poverty and graduation rates
- Racial composition by state
- Police killings by race and gender
- Age distributions and age distributions by race
- The percentage of victims who were under 25
- Whether victims were armed and the types of weapons recorded
- The percentage of victims showing signs of mental illness
- The ten cities with the most recorded police killings
- Race shares among victims in the ten highest-count cities
- A choropleth map of killings by state
- Annual and monthly trends in recorded police killings

## Requirements

- Python 3.10 or newer
- Jupyter Notebook or JupyterLab
- Packages listed in [`requirements.txt`](./requirements.txt)

## Installation

From the project directory, create and activate a virtual environment:

### Windows PowerShell

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

Install the dependencies:

```powershell
python -m pip install -r requirements.txt
```

If PowerShell prevents script activation, run the notebook with the virtual-environment interpreter directly:

```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

## Running the notebook

Start Jupyter from the project directory:

```powershell
python -m notebook
```

Open [`notebook/Fatal_Force_(start).ipynb`](./notebook/Fatal_Force_(start).ipynb) and run the cells from top to bottom. The notebook expects the working directory to be the `notebook` folder because its data paths use `../data/...`.

In VS Code:

1. Open the project folder.
2. Open the notebook.
3. Select the project `.venv` Python interpreter as the kernel.
4. Run all cells in order.

## Data sources

- Police shooting records: The Washington Post's fatal police shooting database, represented in `Deaths_by_Police_US.csv`.
- Socioeconomic and demographic data: U.S. Census data represented in the remaining CSV files.

The data is historical and should not be interpreted as a complete measure of all police encounters or all deaths involving law enforcement. Results depend on the coverage, definitions, and limitations of the source datasets.

## Notes

- Missing values are present in some source columns, particularly household income and victim-level fields.
- Counts describe recorded incidents in the supplied data and are not population-adjusted rates unless explicitly stated.
- The choropleth uses state abbreviations and Plotly's `USA-states` location mode.

## License

No separate project license is currently specified. Review the terms and attribution requirements of the original data providers before redistributing the datasets.
