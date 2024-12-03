# Mutter2024_TheCryosphere
Scripts to reproduce radargrams from Mutter and Holschuh 2024 

DEPENDENCIES
This code has been run using Python 3.8.10. The code utilizes the depth_shift and distance_vector functions from Nick Holschuh's NDH_PythonTools GitHub Repository. 

DESCRIPTION
Dictonary of radar data and corresponding python scripts to reproduce radargrams from Mutter and Holschuh (2024).

Core_Data.mat
  - Dictionary of radar data from 15 historic deep ice core drill sites (Camp Century, GISP2, GRIP, NorthGRIP, DYE-3, NEEM, Vostok, Dome C, Byrd, Siple Dome, WAIS Divide, SPICE, Dome Fuji, EDML, Talos Dome). Each core site has a corresponding dictionary of flights (e.g. Flight_1, Flight_2) and each flight has a corresponding dictionary of radar data and metadata with the following keys:
      - Imdata (nxm array of backscatter power)
      - lat (mx1 array of latitude coordinates for each trace)
      - lon (mx1 array of longitude coordinates for each trace)
      - x_coord (mx1 array of Antarctic Polar Stereographic EPSG:3031 (Antarctic Cores) or Sea Ice Polar Stereographic North EPSG:3413 (Greeland Cores) coordinate for each trace (meters))
      - y_coord (mx1 array of Antarctic Polar Stereographic EPSG:3031 (Antarctic Cores) or Sea Ice Polar Stereographic North EPSG:3413 (Greeland Cores) coordinate for each trace (meters))
      - distance (mx1 array of distance along flight transect in km)
      - filenames (original radar data filenames)
      - time (nx1 array of fast time intervals in seconds)
      - surf_index (mx1 array of indices marking the surface return for each trace)
      - surface_elevation (mx1 array of surface elevation measurements for each trace (m))
      - bed_index (mx1 array of bed elevation measurements for each trace (m))
      - core_coords_latlon (lat,lon coordinates of the core site)
      - core_coords_xy (x,y coordinates of the core site in EPSG:3031 (Antarctica)) or EPSG:3413 (Greenland)
      - core_depth (ice core depth (m))
      - core_path_distance (minimum distance between flight transect and core drill site)
      - core_index (index of trace nearest to the core drill site) 
      - inset_index (indices of traces +/- 5km around the core index. Note that some transects do not extend the full 10 km. 
      - long_profile_index (indices of traces +/- 20 km around the core index. Note that some transects do not extend the full 40 km. 
      - degrees_from_flow (angle between surface velocity vector and inset index flight line vector) 

  - 

- To produce radargrams shown in Figures 3 and 4 run script '.py'. 

REFERENCE
Mutter, E. L. and Holschuh, N. (2024) Advancing interpretation of incoherent scattering in ice penetrating radar data used for ice core site selection. The Cryophere Preprint. doi: 10.5194/egusphere-2024-2450

METADATA
Author: Ellen Lucinda Mutter
Institution: Cornell University
Associated Project: NSF Center for Oldest Ice Exploration (COLDEX)
