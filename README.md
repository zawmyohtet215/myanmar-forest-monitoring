# myanmar-forest-monitoring
A Local-First Big Data Pipeline for Forest Resource Monitoring in Myanmar Using Multi-Source Satellite and Climate Data (2020–2024)


Database:
- PostgreSQL 15
- PostGIS 3.4 (geometry + raster support)

Extensions enabled:
- postgis
- postgis_raster

Step 1 - Create 3 schemas in the database.

- raw
- processed
- analytics
  
CREATE SCHEMA raw;
CREATE SCHEMA processed;
CREATE SCHEMA analytics;

Step 2 — Load Myanmar Administrative Boundaries

Boundaries Shapefile - https://geonode.themimu.info/layers/geonode%3Ammr_polbnda2_adm1_250k_mimu_1

shp2pgsql.exe is installed with PostGIS but its folder is not automatically added to PATH. Need to fix this.

Under User variables (or System variables):
Select Path
Click Edit
Click New
Add this (depending on where the file is): C:\Program Files\PostgreSQL\15\bin
