# DAI Algorithm <img src="/logo.png" align="right" width="200" />
## DAI interpolation method
### Description
Satellite imagery and remote sensing data provide the physical characteristics of the Earth surface from the measures of the radiation reflectance of special cameras. Such a property allows the use of these information for environmental monitoring. However, one of the weaknesses of this appraisal is the spatial and temporal granularity of the information. While some satellite raster products have almost daily information but poor spatial resolution – e.g. Sentinel 3 provides Chl and TSM information at 300 m spatial resolution, or VIIRS and MODIS provides Chl at 750 m and 1000 m resolution, respectively –; aerial image is provided by Sentinel 2 at 10-60 m resolution, but with a temporal granularity of 5 days. Daily Aerial Image (DAI) interpolation method adapts the spatial Inverse Distance Weighting (IDW) method to temporal series for spatial interpolation of the RGB bands of two aerial images in order to obtain interpolated daily images between two dates.
## Installation
•	Download the last version available "last_version.zip".
•	Open QGIS v3.x.
•	Select Plugins\Manage and Install Plugins
•	Select the option Install from ZIP.
•	Browse the route to the “last_version.zip” file and press the install button.
## How does it work
DAI interpolation method needs the following input information:
•	Aerial Image 1: A three-banded (RGB) raster map with the older aerial image that needs to be interpolated.
•	Aerial Image 2: A three-banded (RGB) raster map with the more recent aerial image that needs to be interpolated.
•	Dates: Defines the day/month/year (dd/mm/yyyy) of both, Aerial Image 1 and 2.
•	Area of interest (shp): Defines the outer interpolation polygon with a shape file.
•	Working folder: Defines de destination route.
The program will calculate the intermediate days between dates 1 and 2; and will interpolate the original images according to the temporal distance to them of every single date. 

## Case study
The information provided allows the reproduction of an interpolation example between two Sentinel 2 aerial images of Mar Menor lagoon from 14 and 19 of June of 2022.
<img src="/case_mar_menor.jpeg" width="600" />
## Authors
- [@Pablo Blanco-Gómez](https://orcid.org/0000-0001-9465-2912)
- [@Jose Luis Jimenez Garcia](https://orcid.org/0000-0001-6619-9057)
## Acknowledgments
Authors acknowledge Vicente M. Candela Canales for supporting the R&D investment and programs within the Vielca companies.

