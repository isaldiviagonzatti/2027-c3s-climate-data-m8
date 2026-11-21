# Fire Weather Index (FWI) data for Europe

This folder contains a copy of the data used in the notebook `visualising-fwi-for-esotc.ipynb`. The notebook can download these files from here as a quick alternative to requesting them from the Copernicus Early Warning Data Store (EWDS).

## Source and citation

The data were provided by the [CEMS-EMS European Forest Fire Information System (EFFIS)](https://effis.jrc.ec.europa.eu) of the European Commission Joint Research Centre. They were downloaded from the dataset [Fire danger indices historical data from the Copernicus Emergency Management Service](https://ewds.climate.copernicus.eu/datasets/cems-fire-historical-v1) on the EWDS on 21 November 2026.

If you use these data, please cite:

> Copernicus Climate Change Service, Climate Data Store, (2019): Fire danger indices historical data from the Copernicus Emergency Management Service. Copernicus Climate Change Service (C3S) Climate Data Store (CDS). DOI: [10.24381/cds.0e89c522](https://doi.org/10.24381/cds.0e89c522) (Accessed on 21-NOV-2026)

## Licence

The dataset is distributed under the [Creative Commons Attribution 4.0 International (CC-BY-4.0)](https://creativecommons.org/licenses/by/4.0/) licence. The files here are unchanged: they are exactly what the EWDS returned for the request below.

## Request

One file per year, for the years 2016, 2017, 2018, 2019, 2020 and 2022:

```python
{
    'product_type': 'reanalysis',
    'variable': 'fire_weather_index',
    'system_version': '4_1',
    'dataset_type': 'consolidated_dataset',
    'year': year,
    'month': ['01', '02', ..., '12'],
    'day': ['01', '02', ..., '31'],
    'grid': '0.5/0.5',
    'area': [75, -30, 30, 45],  # North, West, South, East: Europe
    'data_format': 'netcdf',
}
```

Each file holds the daily FWI (variable `fwinx`) for one year on a 0.5° grid over Europe.