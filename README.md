# RGR-pdal-topo
RGR-pdal-topo is an open source project to provide Python modules and tutorial notebooks for processing topographic data for fault scarp and alluvial fan analyses. 

This project is supported by the INTERN supplement to the OpenTopography NSF award at ASU (ID: 1948857) to study active normal fault scarps and alluvial fans in the Rio Grande Rift.

Analyses of fault scarps include the mapping of fault extents from topography and measuring fault throw from topographic profiles. The ages of normal faults can be constrained by dating the alluvial surfaces they modify. Topographic metrics including curvature and roughness serve as proxies for alluvial fan age, as alluvial fans smooth over time. 

This repository provides modules for processing point cloud data into raster grid digital elevation models (DEMs), computing topographic metrics (e.g. slope, curvature, spectral filtering), and performing basic DEM classification for geological mapping. 

We provide Python notebooks demonstrating how to:

- Use PDAL to request data from The National Map and the Entwine Amazon S3 bucket that hosts USGS 3DEP lidar point clouds

- Sample lidar point clouds to create 2D topographic profiles
<img width="220" height="428" alt="image" src="https://github.com/user-attachments/assets/879633b8-a640-4761-9bfb-f4abf1fb5dc7" />


- Generate DEM grids from point clouds using PDAL and GDAL-based python modules
<img width="382" height="368" alt="image" src="https://github.com/user-attachments/assets/b8956ecf-52a5-4441-9d51-89338f6425b0" />


- Compute topographic metrics on DEMs (e.g. surface roughness, slope, curvature, shaded-relief)
<img width="658" height="337" alt="image" src="https://github.com/user-attachments/assets/fd994f5b-7444-4ceb-abab-70aeb34f50a0" />



- Perform basic feature segmentation from DEM derivatives to map fault scarp extents
<img width="370" height="189" alt="image" src="https://github.com/user-attachments/assets/1fc3673f-a6cf-4eba-a320-d66a01bd3a57" />

  
- Create box plots of alluvial fan roughness statistics with geological map GIS layers
<img width="744" height="331" alt="image" src="https://github.com/user-attachments/assets/ee13fa0d-2da5-4852-987f-556e7334053b" />


The provided example notebooks and datasets show analysis of Rio Grande rift normal faults and alluvial fan deposits, however this code is adaptable for use with other study areas. 

** Setup is tested for Windows running Docker & VSCode-Remote Containers

## Required Software:
- Docker Desktop installed
- VScode
- VSCode Extensions: (Local) Docker, Dev Containers, WSL (DEV Container) Python, Pylance, isort, Docker, Jupyter

## Table of contents:
- Dockerfile -- builds a miniconda container for developing in VSCode
- devcontainer -- config files for VSCode Remote Container
- src -- folder containing DEM creation & Analysis Modules, tutorial jupyter_notebooks, test scripts, and testData
## src Table of Contents
- Modules -- folder containing the demAnalysisComponents and demCreationComponents modules
- DEMs -- folder containing the raster and vector data files used in the provided notebook
- geo7x_sangres_all_shp -- shapefile containing GPS points collected for use in the Projecting_GPS_points_to_line notebook
- profiles_for_project -- gps data used in profile notebooks
- testData -- datasets for the tutorial notebooks
- tutorial_notebooks -- notebooks for utilizing AWS point cloud and DEM creation/analysis modules
- ClusterScarp -- notebook demonstrating Kmeans clustering of fault scarp derivative layers
- FanRoughness_Stats -- notebook demonstrating computing and binning roughness values associated with geological map units
- PointCloud_Profiles -- notebook demonstrating plotting and analysis of elevation profiles across fault scarps
- Projecting_GPS_points_to_line -- notebook demonstrating how to project GPS points to a profile line shp

## Getting started:
- Clone this repo
## For VSCode Container setup:
- Launch Docker Desktop & VSCode
- In VSCode, install extensions (listed above)
- Navigate to repo folder
- Select ><, in Remote options, select 'reopen folder in container'
- Once container is launched, add installed VSCode extensions to the Dev container
- Change Python Interpreter to 'Python 3.8 ('rgr':conda) /opt/conda/bin/python'




