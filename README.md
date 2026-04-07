# MODIS_NDVI_Monthly_2016-2024_PierreAuger

**Monthly NDVI (Normalized Difference Vegetation Index) analysis** for the Pierre Auger Observatory region using MODIS satellite data (2016–2024). This repository includes scripts for exporting, visualizing, and plotting NDVI data using Google Earth Engine, Google Colab, and Python.

---

## Features

1. **NDVI Export Script (GeoTIFF)**
   - Exports monthly mean NDVI from MODIS MOD13Q1 (16-day, 250 m resolution).
   - Clips data to the Pierre Auger Observatory bounding box.
   - Outputs one GeoTIFF per month for 2016–2024.

2. **NDVI Thumbnail Visualization (Colab)**
   - Displays monthly NDVI thumbnails directly in Colab.
   - Uses a custom NDVI color palette for clear visualization.
   - Useful for quick inspection of NDVI temporal patterns.

3. **High-Resolution NDVI Maps (Python / Matplotlib / Cartopy)**
   - Plots all 12 months in a 3x4 subplot layout.
   - Overlays Pierre Auger Observatory shapefile and stations of interest.
   - Custom NDVI colormap and gridlines.
   - Saves high-resolution PNG (400 dpi) for reports or presentations.

---

## Requirements

- Python 3.x  
- Google Earth Engine Python API (`earthengine-api`)  
- Google Colab (optional, for thumbnail visualization)  
- `rasterio`, `numpy`, `matplotlib`, `cartopy`  
- Pierre Auger Observatory shapefile (included in `/shapefiles`)  

---

## Usage

### 1. NDVI Export Script
```bash
# Run in Colab or locally with GEE authenticated
python ndvi_export.py

2. NDVI Thumbnail Visualization
# Run in Colab to display monthly NDVI thumbnails
python ndvi_thumbnails.py

3. High-Resolution NDVI Maps
# Run locally to generate monthly maps and save PNG
python ndvi_plot_maps.py

Output
NDVI_01_2016_2024.tif … NDVI_12_2016_2024.tif → Monthly GeoTIFFs
NDVI_Monthly.png → 3x4 subplot figure of all months

License
This repository is licensed under the MIT License. See LICENSE file for details.

Author
Virginia Binet – Doctoral Research on Air Quality and Remote Sensing
