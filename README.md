# SILAM european air quality siulation

A standalone setup for 
Replicates the SILAM CAMS_REG forecast of 20230708.



## Directory content

 EU-short.control            | Control file for 24-h long 0.5x0.5-deg simulation 
 EU.control                  | Control file for 120-h long 0.1x0.1-deg simulation
 README.md                   | This file
 boundary_europe_C_IFS.ini   | Boundary-condition description
 output_config_AQ.ini        | Output-parameter specification



## How to make a simulation



Get the assets (11GB tarball, ~20GB unpacked):
https://silam-testcase-assets.lake.fmi.fi/EU_TEST-assets-20250121.tar.bz2




## Assets file content

|Directory             | Content |
|---|---|
| `boundaries_cifs/`   | Boundary conditions from C-IFS with lumped layers                       | 
| `emis/`              | Emission inventories/files                                              | 
| `meteo/`             | Meteorological fields from operational IFS                              | 
| `photolysis/`        | Photolysis lookup tables (old/new format)                               | 
| `physiography/`      | Physiographic maps                                                      | 
| `output/20230707/`   | Dump and extract from the previous forecast output(initial conditions)  | 
