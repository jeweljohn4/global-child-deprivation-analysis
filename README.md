# Global child deprivation analysis
Analysis and visualization of global child deprivation using UNICEF data
## Table of Contents

- [Introduction](#introduction)
- [Global Distribution: Choropleth Map](#global-distribution-choropleth-map)
- [Top 10 Countries by Average Deprivation](#top-10-countries-by-average-deprivation)
- [Global Trend Over Time](#global-trend-over-time)
- [Gender Differences in Top 10 Countries](#gender-differences-in-top-10-countries)

This page analyzes child deprivation data from UNICEF, focusing on the percentage of children experiencing exactly one severe deprivation. We explore global trends, country-specific data, and gender differences to provide a comprehensive overview of the issue.

# Install required packages
!pip install plotnine geopandas
import pandas as pd
import geopandas as gpd
from plotnine import *

# Load and prepare data
df = pd.read_csv("unicef_indicator_2.csv")
df['year'] = df['time_period'].astype(str).str[:4].astype(int)
#| code-fold: true
