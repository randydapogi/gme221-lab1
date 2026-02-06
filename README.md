# GmE 221 – Laboratory Exercise 1

## Overview

This laboratory sets up a spatial analysis environment using Python and PostGIS and performs a parcel–landuse overlay analysis.

## Environment Setup

- Python 3.x
- PostgreSQL with PostGIS
- GeoPandas, SQLAlchemy, psycopg2

## How to Run

1. Activate the virtual environment
2. Run `main.py` to test the database connection
3. Run `overlay.py` to compute landuse percentages

## Outputs

- PostGIS table: `parcel_landuse_percentage`
- Visualization in QGIS

## Reflection

### Database Connection Milestone

The main.py script should us how data from a PostGIS database can be accessed in a python script using the sqlalchemy library. Data from the database can then be read using the geopandas library. This shows us that we can programmatically retrieve data from a database and perform analysis. This programatic access can enable us to scale up our spatial processing.

### Overlay Analysis Milestone

The overlay.py script read the parcel and landuse table to variable parcel and landuse. A sql query is then executed to get the intersection of parcel and landuse. From the intersection, an sql command is then executed to calculate the summation of area for each land use of each parcel. We then calculated the percentage of each landuse for the parcel and stored the result to a table named parcel_landuse_percentage. This shows us that spatial operations like overlaying can be performed on the tables of the database and the result can then be stored back to the database.
