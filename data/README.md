# Data folder

The data files are not stored on GitHub because they are several gigabytes in total. Running
`notebooks/01_data_collection_and_cleaning.ipynb` recreates them:

- `data/raw/` holds the downloaded files (crashes and people by year, street network, traffic counts,
  mobility data, boundaries and population). Later runs reuse these files instead of downloading again.
- `data/processed/prepared_data.pkl` holds the cleaned datasets that `notebooks/02_analysis.ipynb` loads.
  `data/processed/crash_road_matches.csv` saves the slow crash-to-street matching step from notebook 2.

All sources are public: the City of Chicago Data Portal (https://data.cityofchicago.org) and the
Illinois Department of Transportation's traffic-count service.
