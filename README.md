# Module1 — Weather CSV loader (csv vs pandas)

This repository contains a small Python script (`venv/Module1.py`) that demonstrates two ways to load a CSV file:
- Using Python’s built-in `csv` module
- Using `pandas`


## Project layout

- `venv/Module1.py` — Script that loads the CSV and prints summary info
- `AustraliaWeatherData/Weather Training Data.csv` — Training dataset used by the script
- `AustraliaWeatherData/Weather Test Data.csv` — Additional dataset (not used by default)
- `Module1.html` — Optional documentation generated with `pydoc -w Module1`


## Requirements

- Python 3.8+ (Windows)
- A virtual environment (optional)
- `pandas` Python package

## Quick start (Windows PowerShell)

1) Create and activate a virtual environment:

```powershell
py -m venv venv
.\venv\Scripts\Activate
```

2) Install dependencies into the virtual environment:

```powershell
pip install pandas
```

3) Run the script from the project root (with the venv active):

```powershell
python .\venv\Module1.py
```


## How it works

- `load_csv(file_name)`: Uses `csv.reader` to iterate the file and append rows into a global list `weather_data` via `add_weather_data`.
- `load_csv_pandas(file_name)`: Uses `pd.read_csv` to create a `pandas.DataFrame` and returns it.
- In `__main__`, the script loads `AustraliaWeatherData/Weather Training Data.csv` with both methods, prints row counts, and prints `df.describe()`.

