

**Overview:**  
This project demonstrates how to create a 3D visualization of Sri Lanka's railway network using Digital Elevation Model (DEM) data and OpenStreetMap (OSM) railway data. We will be using R for spatial data processing and 3D rendering with the **rayshader** package.

**Prerequisites:**  
To begin, you will need R and the following libraries:
- **pacman**
- **sf**
- **terra**
- **elevatr**
- **rayshader**
- **scales**
- **tidyverse**


**Steps:**

1. **Install and Load Libraries**  
   Install the required R libraries using `pacman::p_load()`.

2. **Download and Prepare OSM Railway Data for Sri Lanka**  
   Download the OSM railway shapefile for Sri Lanka from **Geofabrik**, unzip it, and load the railway shapefile into R for further processing.

3. **Get Country Boundary Data for Sri Lanka**  
   Download Sri Lanka's country boundary using the **GADM** dataset, which provides the administrative boundaries of the country.

4. **Download Digital Elevation Model (DEM) Data**  
   Obtain DEM data for Sri Lanka, clipped to the country boundary, to represent the elevation of the land surface.

5. **Reproject DEM Data (Optional)**  
   Optionally, reproject the DEM data to the **Lambert Azimuthal Equal Area (LAEA)** projection, which is suitable for creating maps of smaller areas.

6. **Simplify and Filter Railway Data**  
   Filter the railway data to keep only relevant railway classes (e.g., "rail", "narrow_gauge") and simplify the geometry for performance. Reproject the railway shapefile to match the DEM data's coordinate reference system (CRS).

7. **Convert DEM Data to Matrix**  
   Convert the reprojected DEM raster into a matrix format, which is required for the **rayshader** visualization.

8. **Render 3D Map and Overlay Railway Data**  
   Use **rayshader** to create a 3D visualization of the DEM. Overlay the railway network on top of the 3D DEM to create an informative and visually appealing map.

9. **Render and Save High-Quality Image**  
   Save the 3D visualization as a high-quality image with HDR lighting to enhance the details and depth of the rendered scene.



**Conclusion:**  
This project demonstrates how to create a stunning 3D visualization of the railway network in Sri Lanka using DEM and OSM data in R. By following these steps, you can replicate similar visualizations for other regions by modifying the country boundary and OSM data.


**Optional:**  
You can download OSM data for other regions from **Geofabrik** by visiting: [Geofabrik Download](https://download.geofabrik.de/).
