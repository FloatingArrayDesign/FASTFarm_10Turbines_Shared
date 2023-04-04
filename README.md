# Shared Mooring 10-Turbine Array: FAST.Farm Model

This repository contains FAST.Farm inputs files for NREL's 10-turbine shared-mooring array design using the DTU 10 MW spar. The FAST.Farm input files are organized in these directories:
- CommonFiles: shared input files for ElastoDyn, HydroDyn, MoorDyn, and AeroDyn.
- TurbulentWind: inputs for a FAST.Farm run using TurbSim inflow wind (includes turbsim input files)
- SteadyWind: inputs for a FAST.Farm run using steady inflow wind

Please reference the following for detailed information on the design and analysis of this shared-mooring array:
- E. Lozon and M. Hall, “Coupled Loads Analysis of a Novel Shared-Mooring Floating Wind Farm,” Applied Energy, 2022. https://doi.org/10.1016/j.apenergy.2022.120513.
- M. Hall; E. Lozon; S. Housner; S. Sirnivas. “Design and Analysis of a Ten-Turbine Floating Wind Farm with Shared Mooring Lines.” Journal of Physics: Conference Series vol. 2362, 2022. https://doi.org/10.1088/1742-6596/2362/1/012016.

Changes from the input files used in the paper include the following:
- TurbSim Low resolution and high resolution grid sizing, and grid sizing in the farm.fstf file were changed based on guidance from https://github.com/OpenFAST/python-toolbox/tree/main/pyFAST/fastfarm.
	- Low resolution grid spacing changed from 60 m to 25 m
	- Low resolution grid width changed from 10980 m to 7150 m
	- Low resolution grid height changed from 600 m to 575 m 
	- High resolution grid spacing changed from 15 m to 5 m
	- TurbSim time step changed from 0.5 s to 0.1 s
- Simulation length for the TurbulentWind case changed from 4600 seconds to 600 seconds. 
- Open.FAST API changes from OpenFAST v3.0.0 to v3.4.1. See https://openfast.readthedocs.io/en/main/source/user/api_change.html for more information.
