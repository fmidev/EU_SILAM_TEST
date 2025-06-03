# SILAM European air quality simulation

A standalone setup for regional AQ simulation.
Replicates the SILAM CAMS_REG forecast of 20230708.


## Files here


 - `EU-short.control`   Control file for 24-h long 0.5x0.5-deg simulation. Should be runnable
            at not-too-ancient computer within some minutes. Requires about 6GB of RAM. 
 -  `EU.control`       Control file for 120-h long 0.1x0.1-deg simulation, similar to 
                        one provided for CAMS_REGIONAL. Requires some x100 more CPU resources 
                        to complete and about 16 GB of RAM when simulated in a single process.
 - `README.md`                   This file
 -  `boundary_europe_C_IFS.ini`   Boundary-condition description that maps C_IFS species into SILAM ones
 -  `output_config_AQ.ini`        Output-parameter specification



## How to make a simulation


1. Clone the repo

2. Get the assets (11GB tarball, ~20GB unpacked):
https://silam-testcase-assets.lake.fmi.fi/EU_TEST-assets-20250121.tar.bz2

3. Unpack it to the `EU_TEST` directory (the one holding worktree from the EU_TEST repo).

4. Get a working binary for SILAM into some other directory (see https://github.com/fmidev/silam-model)

5. Set `SILAM_INI` environment variable to point to the ini directory from the SILAM worktree:
  `export SILAM_INI=/path/to/silam-model/ini`

5. Run the SILAM binary from the `EU_TEST` directory, giving EU-short. control as a parameter

6. Enjoy the warmth from your CPU

7. The results and log files should come to the `output/AQ_europe_lr_short` directory

8. Use your favourite tools to inspect the output



## Assets file content

|Directory             | Content |
|---|---|
| `boundaries_cifs/`   | Boundary conditions from C-IFS with lumped layers                       | 
| `emis/`              | Emission inventories/files                                              | 
| `meteo/`             | Meteorological fields from operational IFS                              | 
| `photolysis/`        | Photolysis lookup tables (old/new format)                               | 
| `physiography/`      | Physiographic maps                                                      | 
| `output/20230707/`   | Dump and extract from the previous forecast output(initial conditions)  | 
