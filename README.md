# Urban Canvas 🏙️

A data science project that identifies and quantifies visual indicators of urban gentrification by correlating economic data with high-resolution satellite imagery.
This project is going to focus on a couple of slices of Brooklyn instead of the whole borough, I am planning to add more areas once the initial results are in, to for model valadation. 

## 📋 Project Overview

Urban Canvas aims to understand the visual patterns of neighborhood change in Brooklyn, NY by analyzing the relationship between economic indicators and satellite imagery. The project combines:

- **Economic Data Analysis**: Tracking median household income changes across census tracts (2011-2023)
- **Geospatial Visualization**: Mapping economic patterns using census tract boundaries
- **Computer Vision** (Future): Analyzing satellite imagery to identify visual indicators of urban development
- **Machine Learning** (Future): Training models to correlate visual features with economic changes

## 🎯 Objectives

1. **Economic Pattern Analysis**: Map and analyze median household income changes across Brooklyn neighborhoods
2. **Visual Feature Extraction**: Identify visual indicators of gentrification from satellite imagery
3. **Correlation Analysis**: Establish relationships between economic changes and visual urban development patterns
4. **Predictive Modeling**: Develop models to predict neighborhood economic trends from satellite data

## 🛠️ Technology Stack

- **Python**: Core programming language
- **Pandas & GeoPandas**: Data manipulation and geospatial analysis
- **Matplotlib & Seaborn**: Data visualization
- **Rasterio**: Satellite imagery processing
- **PyTorch**: Deep learning framework for computer vision
- **Scikit-learn**: Machine learning utilities
- **Jupyter**: Interactive development and analysis

## 🚀 Quick Start

### Prerequisites

- Python 3.10 or higher
- [uv](https://docs.astral.sh/uv/) package manager

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/tjadryan/urban_canvas.git
   cd urban_canvas
   ```

2. **Create and activate virtual environment:**
   ```bash
   uv venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   uv pip install -e .
   ```

4. **Launch Jupyter:**
   ```bash
   jupyter notebook
   ```

## 📊 Data Sources

### Economic Data
- **Source**: [U.S. Census Bureau](https://data.census.gov)
- **Table**: B19013 (Median Household Income in the Past 12 Months)
- **Geography**: Census tracts in Kings County (Brooklyn), New York
- **Time Periods**: 2011, 2019, 2023 (ACS 5-Year Estimates)
- **Format**: CSV files with metadata

### Geospatial Data
- **Source**: [U.S. Census Bureau Cartographic Boundary Files](https://www.census.gov/geographies/mapping-files/time-series/geo/cartographic-boundary.html)
- **Type**: Census tract boundaries for New York State
- **Scale**: 1:500,000
- **Format**: Shapefile (.shp)

### Satellite Imagery (Future)
- **Source**: To be determined (Google Earth Engine, Planet Labs, or similar)
- **Resolution**: High-resolution imagery for selected neighborhoods
- **Time Periods**: Corresponding to economic data periods

## 📁 Project Structure

```
urban_canvas/
├── README.md                 # Project documentation
├── pyproject.toml           # Project configuration and dependencies
├── gather_data.ipynb        # Main analysis notebook
├── data/                    # Raw data files (not tracked in git)
│   ├── ACSDT5Y20**.csv     # Economic data files
│   ├── *.shp               # Census tract shapefiles
│   └── ...
└── urban_canvas.egg-info/   # Package metadata
```

## 🔬 Analysis Workflow

The primary analysis is contained in `gather_data.ipynb`, which includes:

1. **Data Loading & Cleaning**
   - Import economic data from multiple years
   - Clean and standardize column names
   - Handle missing values and data inconsistencies

2. **Geospatial Processing**
   - Load census tract boundaries
   - Filter for Brooklyn (Kings County) tracts
   - Merge economic data with geographic boundaries

3. **Exploratory Data Analysis**
   - Statistical summaries of income data
   - Temporal analysis of income changes
   - Geographic distribution patterns

4. **Visualization**
   - Choropleth maps of median household income
   - Time series analysis of neighborhood changes
   - Interactive visualizations for data exploration

## 📈 Current Status

### ✅ Completed
- [x] Project setup and environment configuration
- [x] Economic data collection and processing
- [x] Geospatial data integration
- [x] Basic exploratory data analysis
- [x] Initial choropleth visualizations

### 🚧 In Progress
- [ ] Calculate and map percentage change in income between periods
- [ ] Statistical analysis of income trends by neighborhood
- [ ] Identify neighborhoods with significant economic changes

### 🔮 Future Work
- [ ] Identify 5-6 diverse neighborhoods for satellite analysis
- [ ] Acquire high-resolution satellite imagery
- [ ] Develop image preprocessing pipeline
- [ ] Train computer vision models for feature extraction
- [ ] Correlate visual features with economic indicators
- [ ] Build predictive models for neighborhood change

## 🤝 Contributing

This is a learning project, but contributions and suggestions are welcome! Please feel free to:
- Open issues for bugs or feature requests
- Submit pull requests for improvements
- Share feedback on methodology or analysis approaches

## 📝 License

This project is for educational and research purposes. Data sources retain their original licenses and terms of use.

## 👤 Author

**Dominick Ryan**
- Email: tja_dryan@outlook.com
- GitHub: [@TJAdryan](https://github.com/TJAdryan)

## 🙏 Acknowledgments

- U.S. Census Bureau for providing comprehensive economic and geographic data
- The open-source Python data science community for excellent tools and libraries
- Various online resources and tutorials that informed the project methodology