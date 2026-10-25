# MI-TRAP OSM Data Pipeline

**Goal:** An automated data pipeline to fetch OpenStreetMap (OSM) drivable networks for multiple European cities and integrate spatial sensor data via map-matching. Built as a 2-day learning project to practice Python, OSMnx, and GeoPandas workflows for the MI-TRAP project application.

## How to Run
1. Clone this repository.
2. Create the environment:
   `conda create -n mitrap -c conda-forge python=3.12 osmnx geopandas pandas`
   `conda activate mitrap`
3. Run `python fetch_network.py` to download, clean, and export the OSM network data (GraphML and GeoPackage) for Munich and Zurich.
4. Run `python match_sensors.py` to load mock sensor coordinates around the TUM campus and match them to the nearest OSM road segments.

## Limitations
* Currently uses mock sensor coordinates for Munich, as open-source traffic sensor data for the case-study cities requires further portal exploration.
* Network matching relies on simple nearest-edge distance; complex trajectory matching is not implemented.
