# Rain Data Analysis (Python)

Analysis of about 6.5 months of minute-by-minute rain sensor data (May to Nov 2026), done with Python.

## What this project does
- Reads hourly text files (one record per minute, values separated by semicolons)
- Cleans the data: removes error lines, wrong clock dates (sensor restart) and a file with a bad encoding
- Converts time from UTC to IST
- Finds daily and monthly rain totals
- Checks data quality: missing days and incomplete days
- Detects rain events (a dry gap of 60 minutes separates two events) and plots rain intensity with cumulative rain

## Key results
- 229,242 minute records, 172 days with data
- Wettest month: July 2026 (about 291 mm)
- Largest event: 8-9 July 2026 (about 126 mm)
- Highest 1-minute intensity: about 227 mm/h
- About 27 days have no data at all, so some monthly totals are lower than the real rainfall

## Files
- `rain_data_analysis_clean.ipynb` : the code (Jupyter notebook)
- `events_summary.csv` : all detected rain events
- `sample_event_2026-07-28.csv` : data of one event, as a sample
- `graphs/` : plots of the 5 largest events

## Tools
Python, pandas, matplotlib, Jupyter Notebook

The raw data is not shared in this repository.
