---
title: Clipping Rasters - Export Data
parent: Clipping Rasters in ArcGIS Pro
layout: default
nav_order: 8
---

### **Clipping Rasters - Export Data**

You can also zoom to the extent you wish to be working on and clip your dataset based on your zoomed extent. Let's say you are specifically interested in Toronto's islands and port lands.

First, zoom to the islands and port lands.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_018.png' | relative_url }}' alt='Map zoomed into the Toronto's islands and port lands.' title='' width='100%' height='100%' />

Then, right-click on the raster layer you wish to clip from. **Choose Data → Export Data...**

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_019_0.png' | relative_url }}' alt='Contents pane showing the Export Raster tool, found by expanding the Data dropdown menu.' title='' width='100%' height='100%' />

In the Export Raster Data setup window underneath the header "Clipping Geometry", make sure you select **"Current Display Extent"** to only export the data within your zoomed dataframe. You can keep the Spatial Reference same as the original one.

You can also choose to export the raster file as the same format as the original dataset (TIFF). Saving the raster file as a TIFF could also avoid compressing the dataset.

Make sure you save the exported file to your working directory.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_020_3.png' | relative_url }}' alt='Export Raster window with selected Output Format as TIFF and Clipping Geometry set to "Current Display Extent".' title='' width='75%' height='75%' />

Add your exported layer the map area. Your clipped layer should look similar to this.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_021.png' | relative_url }}' alt='Clipped DEM on Former Municipality Boundaries layer.' title='' width='100%' height='100%' />