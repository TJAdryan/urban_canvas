Project Urban Canvas 🏙️
This project aims to identify and quantify the visual indicators of urban gentrification by correlating economic data with high-resolution satellite imagery. The initial analysis focuses on tracking changes in median household income across different neighborhoods in Brooklyn, NY, between 2011 and 2023.

Setup
This project uses uv for environment and package management.

Clone the repository:

Bash

git clone https://github.com/tjadryan/urban_canvas.git
cd urban-canvas
Create the virtual environment:

Bash

uv venv
Activate the environment:

Bash

source .venv/bin/activate
Install dependencies:
All required packages are listed in pyproject.toml. Install them with:

Bash

uv pip install -e .
Data
The raw data is not tracked in this repository and must be downloaded manually into the /data folder.

Geospatial Data:

Source: U.S. Census Bureau Cartographic Boundary Files

File: Shapefile (.shp) for Census Tracts in New York at the 1:500,000 scale.

Economic Data:

Source: data.census.gov

Table: B19013 (Median Household Income) for all census tracts in Kings County, New York.

Files: Downloaded as CSV for three periods: 2011, 2019, and 2023 (using ACS 5-Year Estimates).

Current Status
The initial data processing is complete. The Jupyter notebook 01-data-exploration.ipynb contains the workflow for:

Loading, cleaning, and merging the three income data files.

Loading the census tract shapefile and filtering it for Brooklyn (Kings County).

Merging the final income data with the geospatial data.

Generating a choropleth map visualizing the 2023 median household income.

Next Steps
[ ] Calculate and map the percentage change in income between 2011-2019 and 2019-2023.

[ ] Identify a diverse set of 5-6 neighborhoods for in-depth satellite image analysis.

[ ] Begin acquisition of high-resolution satellite imagery for the selected neighborhoods and time periods.

[ ] Develop the pipeline for slicing satellite images into uniform tiles.

[ ] Train a computer vision model to extract features from the image tiles.

[ ] Correlate the extracted visual features with the observed economic changes.