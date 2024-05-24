# species

The code in this repository is intended to clean a modeled SGCN species richness dataset by standardizing species ID codes, coordinate reference systems, column names, and filenames across multiple input shapefiles. Species ID lists are exported as CSVs to provide base files for crosswalking to common names and scientific names. Cleaned shapefiles are re-exported for uploading onto SNAP's server for public access. 

The cleaned files are located [here](http://data.snap.uaf.edu/data/Base/Other/Species/). All SGCN data is also combined into a long-format table that can be used to query species IDs by HUC and species type (zipped as `tbl/huc_species_lookup.csv.zip` in this repo). Though it contains no meaningful geospatial data, this file was exported as a shapefile for SNAP to host on GeoServer where the species information can be easily queried (zipped as `export/huc_species_lookup.shp.zip` in this repo). 

### Data Source

The original data was created as part of an Alaska Department of Fish and Game State Wildlife Grant project titled "Baseline biodiversity heat maps and climate correlates for Alaska’s Species of Greatest Conservation Need" (C-SWG-1-2021). The principal investigator was Dr. Andy Baltensperger (University of Alaska Fairbanks), with cooperators Dr. Nancy Fresco (University of Alaska Fairbanks), Dr. Julie Hagelin (Alaska Department of Fish and Game), and Ms. Heather McFarland (University of Alaska Fairbanks). Since the original input files are quite large, they are not included in this repo. If you'd like to run this code, you will need to contact the dataset author for access to the original files. 

### To run this code:

You will need an computing environment capable of running Jupyter notebooks, with `pandas` and `geopandas` python packages installed. All code is contained in the `clean_explore_and_export_species_data.ipynb` notebook. The last few cells of the notebook contain a basic function to pull species data given any HUC ID as input. This is the functionality that may potentially be included in some of SNAP's online tools.
