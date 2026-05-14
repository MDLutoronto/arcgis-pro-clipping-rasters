---
title: Clipping Rasters - Using toolboxes
parent: Clipping Rasters in ArcGIS Pro
layout: default
nav_order: 9
---

### **Clipping Rasters - Using toolboxes**

The first method to clip a raster is by using the Data Management toolbox in ArcGIS Pro. Click on Tools in the Analysis tab found in the ribbon at the top of your screen. This should open up the Geoprocessing pane.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_014_0.png' | relative_url }}' alt='In the ribbon, the Tools button can be found in the Analysis tab.' title='' width='100%' height='100%' />

In ArcGIS Pro, there are two different clipping tools for vector and raster datasets. To find the Clip tool that's specifically designed for raster dataset, follow this directory: **Toolboxes  → Data Management Tools  → Raster  → Raster Processing  → Clip Raster.** Alternatively, you can use the *Find Tools* search bar at the top of the geoprocessing pane and type out "**Clip Raster**".

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_015.png' | relative_url }}' alt='Geoprocessing pane showing the location of the Clip Raster tool found by navigating to the Raster and Raster Processing tabs in Data Management Tools' title='' width='35%' height='35%' />

Open the Clip Raster tool. The **Input Raster** should be the Digital Elevation Model we downloaded. Set up the City of Toronto Former Municipality Boundaries file as the **Output Extent**. You can also manually adjust the extent of the rectangle by changing the X Max/Min and Y Max/Min numbers.

The Clipping tool will clip your raster dataset to a rectangle that covers your extent. If you want your clipped raster data to be **exact same shape as the clipping layer** (the City boundaries, in this case), make sure you check the "**Use Input Features for Clipping Geometry (optional)**" box.

In the Output Raster Dataset, save your output dataset to your preferred directory.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_016.png' | relative_url }}' alt='Clip Raster window where the "Use Input Features for Clipping Geometry" has been selected.' title='' width='100%' height='100%' />

Click OK after all settings are properly changed.

Note: every time you click on one of the settings, the **Tool Help panel** on the right will show you a detailed explanation of this option. You can read through if you are needs clarification with some of the options.

After the clipping process is completed, the clipped layer should be added to display automatically. If not, find your clipped dataset under the folder you chose to export the data in the ArcCatalog panel, and add it to the map.

The clipped raster dataset should look similar to the following image.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_017.png' | relative_url }}' alt='DEM clipped to the size of the Toronto Municipality Boundaries layer.' title='' width='100%' height='100%' />  